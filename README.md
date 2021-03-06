# Numpy.org

## Getting Started

To contribute to the website, you'll first need to install the *extended
version* of Hugo.

The Hugo [install page](https://gohugo.io/getting-started/installing/) has
instructions for different platforms and installers; make sure you end up with
the extended version.

On Linux it may be easiest to pick up a tarball of the latest extended version
from the [release page](https://github.com/gohugoio/hugo/releases/) and
install it per https://gohugo.io/getting-started/installing/#install-hugo-from-tarball.

Next, clone this repository, and install the theme:

```
git submodule update --init
```

The development web server is started with:

```
hugo server
```

or

```
hugo server -D
```

to run the hugo server with draft enabled.

after which the site should be served at http://localhost:1313.

You'll see
```
error: failed to transform resource: TOCSS: failed to transform "style.sass"
```
if you don't have the Hugo extended version.


## Using docker:

* Build the docker image:

```

  $ docker build -t deploy_surge .
  $ docker images

```

Run the image:

```
  $ docker run -e SURGE_LOGIN=${SURGE_LOGIN} -e SURGE_TOKEN=${SURGE_TOKEN} -e PR_NUMBER=${TRAVIS_PULL_REQUEST} deploy_surge
```

Note: `SURGE_LOGIN` and `SURGE_TOKEN` is needed only when you want to push the
build in surge server. The URL will look like: numpy-${PR_NUMBER}.surge.sh

So you can use some random number instead of `TRAVIS_PULL_REQUEST` variable.

You also can run the docker image in daemon mode and then interact with the container and run the hugo server.

## User Experience (UX)

### NumPy Color Palette

#FFC553 Mustard
#4DABCF Maximum Blue
#4D77CF Han Blue
#FFFFFF White
#EEEEEE Isabelline
#6C7A89 Aurometalsaurus
#013243 Warm Black
