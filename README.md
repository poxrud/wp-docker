# WP-Docker 
A Simple Docker Stack file for local WordPress Development. 
Launches php, mysql, phpmyadmin and WordPress.


## Prerequisites
Please make sure that you have Docker installed and running. 
On my mac I installed it using: 

``` 
brew cask install docker 
```

## Installation 
### Initialize a Swarm
You only need to do this once on your development machine. 

```
docker swarm init
```

### Map the wp-content folder to a local folder on your dev machine
Edit stack.yml and replace _/Users/phil/Projects/Docker/storage/_ with the full path to your local folder. 

## Running the stack
```
docker stack deploy -c stack.yml my-wp
```
Replace _my-wp_ with any other name. 

## Access WordPress and phpMyAdmin
WordPress ``` http://localhost:8080 ```

phpMyAdmin ``` http://localhost:8081 ```


## Shutdown the stack
```
docker stack rm my-wp
```

## Author
Phil Oxrud
Twitter: [@poxrud](https://www.twitter.com/poxrud)
