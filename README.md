# docker-rhel-installation

```bash
sudo yum update -y
```

```bash
sudo yum install -y yum-utils device-mapper-persistent-data lvm2
```

```bash
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```
Remove existing runtimes:


```bash
sudo yum remove podman
```

Similarly:

```bash
sudo yum remove buildah
```
```bash
sudo yum install -y docker-ce
```

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

```bash
sudo docker --version
```

# For docker-compose

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

```bash
sudo chmod +x /usr/local/bin/docker-compose
```

```bash
docker-compose --version
```

Add docker user:

```bash
sudo usermod -aG docker $USER
```

```bash
sudo chmod 666 /var/run/docker.sock
```
