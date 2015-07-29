### [dnsmasq](http://www.thekelleys.org.uk/dnsmasq/doc.html) Docker container

This image is based on the [Glider Lab's Alpine](https://registry.hub.docker.com/u/gliderlabs/alpine) lightweight Docker image.

This Docker image expects you to BYOCF (Bring Your Own Config File) as there are some
configuration settings that depend on several things in your environment.

Simply drop your `dnsmasq.conf` file on the same directory where you're building
the Docker image. There is an `ONBUILD` callback that, when triggered, will
copy it to where `dnsmasq` expects it to be (`/etc/dnsmasq.conf`) inside the container.
