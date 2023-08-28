Don't worry if you get stuck. This is mostly a learning exercise. I'll provide more rigorous backend training in the future.

# Create a virtual machine

* Ubuntu 22.04
* Use a small instance type. Just 2 cores/2 GB memory or similar. Give it a relatively large (160GB+) storage volume in order to handle the iobio backend data.


# Install docker

* Instructions [here](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)


# Try running the iobio backend in docker on the VM

* Instructions [here](https://github.com/iobio/iobio-gru-backend)

# Extra credit - Try building gene.iobio to use your custom backend

This one is tricky because I don't think gene.iobio works without TLS anymore, so you'll need to set up DNS records and some sort of a reverse proxy on your VM. If you want to give this a shot:

* Use [route53](https://aws.amazon.com/route53/) to point an iobio subdomain at your VM's IP address
* Learn a bit about [reverse proxies](https://www.cloudflare.com/learning/cdn/glossary/reverse-proxy/)
* Try running the [Caddy](https://caddyserver.com/) reverse proxy. It will automatically get you a TLS certificate
* Build gene.iobio to point at your VM's domain

# Delete the VM (and the volume(s))
