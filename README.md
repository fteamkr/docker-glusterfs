

- https://github.com/gluster/gluster-containers
- https://www.youtube.com/watch?v=4Xf8pmDEZYw
- https://www.slideshare.net/slideshow/gluster-containers/62778458
- https://gist.github.com/scyto/f4624361c4e8c3be2aad9b3f0073c7f9
- https://github.com/gluster/gluster-containers/pkgs/container/gluster-containers
- https://gist.github.com/scyto/452fc778c4c3ba7caf03b833151e84a1


```
sudo docker pull ghcr.io/gluster/gluster-containers:fedora

sudo docker network create --scope=swarm --attachable -d overlay storage-network

sudo docker run -v /etc/glusterfs:/etc/glusterfs:z -v /var/lib/glusterd:/var/lib/glusterd:z -v /var/log/glusterfs:/var/log/glusterfs:z -v /sys/fs/cgroup:/sys/fs/cgroup:rw -d --privileged=true -v /dev/:/dev --cgroupns=host ghcr.io/gluster/gluster-containers:fedora

sudo docker plugin install --alias glusterfs originnexus/glusterfs-plugin
```
