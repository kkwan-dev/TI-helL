# DOCKER COMMAND REMOTE EXECUTION CONFIG

## How to Set

```sh
sudo vi /lib/systemd/system/docker.service


# docker.service configuration file
  ...
  # modify ExecStart config
  ExecStart=/usr/bin/dockerd -H unix:///var/run/docker.sock -H {HOST_IP}:2375
  ...

# docker daemon and service restart
sudo systemctl daemon-reload
sudo systemctl restart docker.service
```

## How to Use

```sh
docker -H [TARGET_HOST_IP] [COMMAND]
```
