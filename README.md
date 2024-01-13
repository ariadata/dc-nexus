# gitlab-ce with docker-compose
[![Build Status](https://raw.githubusercontent.com/ariadata/ariadata-files/main/public-assets/images/ariadata_logo.png)](https://ariadata.co)

![](https://img.shields.io/github/stars/ariadata/dc-nexus.svg)
![](https://img.shields.io/github/watchers/ariadata/dc-nexus.svg)
![](https://img.shields.io/github/forks/ariadata/dc-nexus.svg)

### This needs [docker , docker-compose](https://github.com/ariadata/dockerhost-sh) Installed

---
## 1- Clone the repository
```bash
git clone -b main https://github.com/ariadata/dc-nexus.git && cd dc-nexus
```

## 2- Create `data` directory
```bash
mkdir -p data && chmod -R 777 data
cp .env.example .env
```

## 3- Modify `.env` file if you need

## 4- Run the stack:
```bash
docker compose up -d
```

## 5- Wait about 10 sec , then run this to get the initial admin password:
```bash
cat data/admin.password
```

## 6- Open `http://IP_ADDRESS:8081` in your browser


## Additonal Configurations and Information:
### Docker Hub Proxy
To set up a proxy to Docker Hub:

**For the blob storage**
- Click the config (gear) icon.
- Navigate to 'Blob Stores'.
- Create a new Blob Store of type File.
    - You can name it whatever you like, but a good choice is `docker-hub`.
- Click 'Create Blob Store'.

**For the Security Realm**
- Click Security > Realms
- Add the 'Docker Bearer Token Realm'
- Click 'Save'

**For the repo itself**
- Click 'Repositories'
- Click 'Create Repository' and select 'docker (proxy)'
- Give it some name (`docker-hub-proxy`)
- Check 'HTTP' and give it a valid port (`8082`)
- Check 'Allow anonymous docker pull'
- Under Proxy > Remote Storage, enter this url: `https://registry-1.docker.io`
- Under Docker Index, select 'Use Docker Hub'
- Under Storage > Blob Store, select the blob store you created earlier (`docker-hub`)
- Click 'Create Repository'

#### Docker configuration
For Docker Desktop (Windows or macOS), open your Docker Preferences, and select 'Docker Engine'.

Add this sections into the json file `/etc/docker/daemon.json`:
```
  "insecure-registries": ["IP_ADDRESS:8082"],
  "registry-mirrors": ["http://IP_ADDRESS:8082"]
```

```
  "registry-mirrors": ["https://docker-proxy.domain.net"]
```

Apply & Restart

#### Pulling Through the Proxy
You can now pull images via your repository.  If the image you want is not in your local repo, it'll be pulled from docker hub and cached into your repo for the default amount of time (24 hours) before being re-checked.

An example pull:

```
docker pull IP_ADDRESS:8082/ubuntu
```

### Private Docker Repository
**For the blob storage**
- Click the config (gear) icon.
- Navigate to 'Blob Stores'.
- Create a new Blob Store of type File.
    - You can name it whatever you like, but a good choice is `docker-private`.
- Click 'Create Blob Store'.

**For the repo itself**
- Click 'Repositories'
- Click 'Create Repository' and select 'docker (hosted)'
- Give it some name (`docker-private`)
- Check 'HTTP' and give it a valid port (`8083`)
- Under Docker Index, select 'Use Docker Hub'
- Under Storage > Blob Store, select the blob store you created earlier (`docker-private`)
- Click 'Create Repository'

**Docker Config**

Make sure you add the new url and port to the `insecure-registries` section of the docker config.

Eg:

```
  "insecure-registries": [
    "IP_ADDRESS:8082",
    "IP_ADDRESS:8083"
  ],
```

#### Docker Login
To connect to the repository, you will need to login using the docker cli:

```
docker login IP_ADDRESS:8083
```

You can then provide user credentials (eg. - the admin user will work).

#### Tagging private images
When you build a docker impage you'd like to push to the private registry, be sure to prefix the image name with the registry url.

Example:

```
docker build -t IP_ADDRESS:8083/myimage:latest .
```

Once it has been built, you can push it to the registry:

```
docker push IP_ADDRESS:8083/myimage:latest
```

### for composer .json
update `composer.json` file in your project root directory and add the following lines in the:
```
"repositories": [
	{
	  "type": "composer",
	  "url": "https://composer-proxy.youdromin.com/repository/composer-proxy/"
	},
	{
	  "packagist.org": false
	}
]
```
