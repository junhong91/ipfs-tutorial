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

## 2. Project Setup:

```sh
ipfs init
ipfs daemon
```

That will start your IPFS server locally. Lastly we need to configure IPFS to allow CORS. We will have to stop the ipfs (ctrl- c) and modify a few things:

```sh
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods '["PUT", "GET", "POST", "OPTIONS"]'
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '["*"]'
ipfs daemon
```

## 3. Hosting a Website:

gist is [here](https://gist.github.com/sogoiii/e07ff464c4ff8a6fa9daa0ca927af3cb)

copy the `index.html` into your project folder and run node

```sh
sudo npm install http-server -g
http-server -p 1337
```

## Reference

- [Uploading an Image to IPFS](https://github.com/junhong91/ipfs-tutorial.git)
- [Install IPFS on localhost](https://docs.ipfs.tech/how-to/websites-on-ipfs/single-page-website/#install-ipfs-desktop)
