## PHP Formatter - provide some bulk actions for your PHP projects to ensure their consistency
[![Docker Pulls](https://img.shields.io/docker/pulls/rvannauker/php-formatter.svg)](https://hub.docker.com/r/rvannauker/php-formatter/) [![Docker Stars](https://img.shields.io/docker/stars/rvannauker/php-formatter.svg)](https://hub.docker.com/r/rvannauker/php-formatter/) [![](https://images.microbadger.com/badges/image/rvannauker/php-formatter:latest.svg)](https://microbadger.com/images/rvannauker/php-formatter:latest) [![GitHub issues](https://img.shields.io/github/issues/RichVRed/docker-php-formatter.svg)](https://github.com/RichVRed/docker-php-formatter) [![license](https://img.shields.io/github/license/RichVRed/docker-php-formatter.svg)](https://tldrlegal.com/license/mit-license)

Docker container to install and run php-formatter

### Installation / Usage
1. Install the rvannauker/php-formatter container:
```bash
docker pull rvannauker/php-formatter
```
2. Run php-formatter through the php-formatter container:
```bash
sudo docker run --rm --volume $(pwd):/workspace --name="php-formatter" "rvannauker/php-formatter" formatter:use:sort {destination}
```
```bash
sudo docker run --rm --volume $(pwd):/workspace --name="php-formatter" "rvannauker/php-formatter" formatter:strict:fix {destination}
```
```bash
sudo docker run --rm --volume $(pwd):/workspace --name="php-formatter" "rvannauker/php-formatter" formatter:header:fix {destination}
```

### Download the source:
To run, test and develop the PHP-FORMATTER Dockerfile itself, you must use the source directly:
1. Download the source:
```bash
git clone https://github.com/RichVRed/docker-php-formatter.git
```
2. Build the container:
```bash
sudo docker build --force-rm --tag "rvannauker/php-formatter" --file php-formatter.dockerfile .
```
3. Test running the container:
```bash
 $ docker run rvannauker/php-formatter --help
```