# Firstly install WSL

Open powershell and run:

```shell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

# install Ubuntu

Open windows store and install ubuntu 16.04 LTS.

then open bash and wait until installation finished.

Then create user and password.

Then switch to root user.

```shell
sudo su
```

# install R

```shell
vim /etc/apt/sources.list
```
and then add the line, this is to install R3.5

```shell
deb https://cloud.r-project.org/bin/linux/ubuntu xenial-cran35/
```

Then run the following to install R

```shell
apt-get update
apt-get install r-base
```

# install R packages

```shell
> install.packages('ggplot2')
```

# Testing running Rscript

```shell
Rscript test.r
```

# Scheduling using crontab

find where Rscript is:
```shell
which Rscript
```
Then

```shell
crontab -e
```
adding the following line

```shell
* * * * * /path/to/Rscript /path/to/Rfile >> /path/to/log/file 2>&1
```

# Almost done
Check if it is scheduling:
```shell
service start cron
```
if working write it in the .bashrc
Next time you open the bash, it will run the scheduling.
remember to sign in with root user:

```shell
sudo su
```
