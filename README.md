# docker-logrotate
Truncates container logs when they grow in size

## Usage

docker run -d -v /var/lib/docker/containers:/var/lib/docker/containers -v /var/log/docker:/var/log/docker -e "LOGS_DIRECTORIES=/var/lib/docker/containers /var/log/docker" -e "LOGROTATE_SIZE=100M" barcond/logrotate:1
