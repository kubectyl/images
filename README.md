# Images

A curated collection of core images that can be used with Kubectyl Rocket system. Each image is rebuilt
periodically to ensure dependencies are always up-to-date.

Images are hosted on `ghcr.io` and exist under the `games`, `installers`, and `images` spaces. The following logic
is used when determining which space an image will live under:

* `oses` — base images containing core packages to get you started.
* `games` — anything within the `games` folder in the repository. These are images built for running a specific game
or type of game.
* `installers` — anything living within the `installers` directory. These images are used by install scripts for different
Rockets within Kubectyl, not for actually running a game server. These images are only designed to reduce installation time
and network usage by pre-installing common installation dependencies such as `curl` and `wget`.
* `images` — these are more generic images that allow different types of games or scripts to run. They're generally just
a specific version of software and allow different Rockets within Kubectyl to switch out the underlying implementation. An
example of this would be something like Java or Python which are used for running bots, Minecraft servers, etc.

All of these images are available for `linux/amd64` and `linux/arm64` versions, unless otherwise specified, to use
these images on an arm64 system, no modification to them or the tag is needed, they should just work.

## Contributing

When adding a new version to an existing image, such as `java v42`, you'd add it within a child folder of `java`, so
`java/42/Dockerfile` for example. Please also update the correct `.github/workflows` file to ensure that this new version
is tagged correctly.

## Available Images

* [`base oses`](https://github.com/kubectyl/images/tree/master/oses)
  * [`alpine`](https://github.com/kubectyl/images/tree/master/oses/alpine)
    * `ghcr.io/kubectyl/images:alpine`
  * [`debian`](https://github.com/kubectyl/images/tree/master/oses/debian)
    * `ghcr.io/kubectyl/images:debian`
* [`games`](https://github.com/kubectyl/images/tree/master/games)
  * [`rust`](https://github.com/kubectyl/images/tree/master/games/rust)
    * `ghcr.io/kubectyl/games:rust`
  * [`source`](https://github.com/kubectyl/images/tree/master/games/source)
    * `ghcr.io/kubectyl/games:source`
* [`golang`](https://github.com/kubectyl/images/tree/master/go)
  * [`go1.14`](https://github.com/kubectyl/images/tree/master/go/1.14)
    * `ghcr.io/kubectyl/images:go_1.14`
  * [`go1.15`](https://github.com/kubectyl/images/tree/master/go/1.15)
    * `ghcr.io/kubectyl/images:go_1.15`
  * [`go1.16`](https://github.com/kubectyl/images/tree/master/go/1.16)
    * `ghcr.io/kubectyl/images:go_1.16`
  * [`go1.17`](https://github.com/kubectyl/images/tree/master/go/1.17)
    * `ghcr.io/kubectyl/images:go_1.17`
* [`java`](https://github.com/kubectyl/images/tree/master/java)
  * [`java8`](https://github.com/kubectyl/images/tree/master/java/8)
    * `ghcr.io/kubectyl/images:java_8`
  * [`java8 - OpenJ9`](https://github.com/kubectyl/images/tree/master/java/8j9)
    * `ghcr.io/kubectyl/images:java_8j9`
  * [`java11`](https://github.com/kubectyl/images/tree/master/java/11)
    * `ghcr.io/kubectyl/images:java_11`
  * [`java11 - OpenJ9`](https://github.com/kubectyl/images/tree/master/java/11j9)
    * `ghcr.io/kubectyl/images:java_11j9`
  * [`java16`](https://github.com/kubectyl/images/tree/master/java/16)
    * `ghcr.io/kubectyl/images:java_16`
  * [`java16 - OpenJ9`](https://github.com/kubectyl/images/tree/master/java/16j9)
    * `ghcr.io/kubectyl/images:java_16j9`
  * [`java17`](https://github.com/kubectyl/images/tree/master/java/17)
    * `ghcr.io/kubectyl/images:java_17`
  * [`java17 - OpenJ9`](https://github.com/kubectyl/images/tree/master/java/17j9)
    * `ghcr.io/kubectyl/images:java_17j9`
  * [`java18`](https://github.com/kubectyl/images/tree/master/java/18)
    * `ghcr.io/kubectyl/images:java_18`
  * [`java18 - OpenJ9`](https://github.com/kubectyl/images/tree/master/java/18j9)
    * `ghcr.io/kubectyl/images:java_18j9`
* [`nodejs`](https://github.com/kubectyl/images/tree/master/nodejs)
  * [`node12`](https://github.com/kubectyl/images/tree/master/nodejs/12)
    * `ghcr.io/kubectyl/images:nodejs_12`
  * [`node14`](https://github.com/kubectyl/images/tree/master/nodejs/14)
    * `ghcr.io/kubectyl/images:nodejs_14`
  * [`node15`](https://github.com/kubectyl/images/tree/master/nodejs/15)
    * `ghcr.io/kubectyl/images:nodejs_15`
  * [`node16`](https://github.com/kubectyl/images/tree/master/nodejs/16)
    * `ghcr.io/kubectyl/images:nodejs_16`
  * [`node17`](https://github.com/kubectyl/images/tree/master/nodejs/17)
    * `ghcr.io/kubectyl/images:nodejs_17`
  * [`node18`](https://github.com/kubectyl/images/tree/master/nodejs/18)
    * `ghcr.io/kubectyl/images:nodejs_18`
* [`python`](https://github.com/kubectyl/images/tree/master/python)
  * [`python3.7`](https://github.com/kubectyl/images/tree/master/python/3.7)
    * `ghcr.io/kubectyl/images:python_3.7`
  * [`python3.8`](https://github.com/kubectyl/images/tree/master/python/3.8)
    * `ghcr.io/kubectyl/images:python_3.8`
  * [`python3.9`](https://github.com/kubectyl/images/tree/master/python/3.9)
    * `ghcr.io/kubectyl/images:python_3.9`
  * [`python3.10`](https://github.com/kubectyl/images/tree/master/python/3.10)
    * `ghcr.io/kubectyl/images:python_3.10`

### Installation Images

* [`alpine-install`](https://github.com/kubectyl/images/tree/master/installers/alpine)
  * `ghcr.io/kubectyl/installers:alpine`

* [`debian-install`](https://github.com/kubectyl/images/tree/master/installers/debian)
  * `ghcr.io/kubectyl/installers:debian`
