# docker-postgres

A simple postgres setup with docker compose

# How to use it

- Install docker with you preferred method. Suggestion for Linux users: `curl -fsSL https://get.docker.com/ | sudo sh -`
- (Optional) Recommended: Add your user to `docker` group: `sudo usermod -aG docker <YOUR_USERNAME>`. You need to restart
- Install compose
```sh
DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
mkdir -p $DOCKER_CONFIG/cli-plugins
curl -SL https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64 -o $DOCKER_CONFIG/cli-plugins/docker-compose
```
- Start postgres: `docker compose up -d`
- The following command should work now: `docker compose exec postgres psql -U banana --password -c 'SELECT 1;'`
