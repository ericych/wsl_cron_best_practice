# Firstly install WSL

# install Ubuntu
# install R

```shell
sudo vim /etc/apt/sources.list
```
and then add the line, this is to install R3.5

```shell
deb https://cloud.r-project.org/bin/linux/ubuntu xenial-cran35/
```

Then run the following to install R

```shell
sudo apt-get update
sudo apt-get install r-base
```
