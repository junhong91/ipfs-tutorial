# IPFS(Interplanetary Files System) Tutorial

## 1. Install IPFS on local host(Linux)

1. Download the Linux binary from dist.ipfs.tech

```sh
wget https://dist.ipfs.tech/kubo/v0.15.0/kubo_v0.15.0_linux-amd64.tar.gz
```

2. Unzip the file:

```sh
tar -xvzf kubo_v0.15.0_linux-amd64.tar.gz

> x kubo/install.sh
> x kubo/ipfs
> x kubo/LICENSE
> x kubo/LICENSE-APACHE
> x kubo/LICENSE-MIT
> x kubo/README.md
```

3. Move into the `kubo` folder and run the install script:

```sh
cd kubo
sudo bash install.sh

> Moved ./ipfs to /usr/local/bin
```

4. Test that IPFS has installed correctly:

```sh
ipfs --version

> ipfs version 0.15.0
```

## Reference

[Uploading an Image to IPFS](https://github.com/junhong91/ipfs-tutorial.git)
[Install IPFS on localhost](https://docs.ipfs.tech/how-to/websites-on-ipfs/single-page-website/#install-ipfs-desktop)
