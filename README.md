# heroku-buildpack-mozjpeg-encoder
A [buildpack](https://devcenter.heroku.com/articles/buildpacks) that reduces the size of JPEG files in Heroku apps using [mozjpeg](https://github.com/mozilla/mozjpeg).

## Usage

1. Enable [Heroku buildpack multi](https://github.com/heroku/heroku-buildpack-multi).

    ```
    $ heroku config:add BUILDPACK_URL=https://github.com/heroku/heroku-buildpack-multi
    ```

2. Create text file named `.buildpacks` in the root of your application. Its contents should be:
    1. For Ruby and Rails

        ````
        https://github.com/michrome/heroku-buildpack-mozjpeg-encoder
        https://github.com/heroku/heroku-buildpack-ruby
        ````

    2. For Node.js

        ````
        https://github.com/michrome/heroku-buildpack-mozjpeg-encoder
        https://github.com/heroku/heroku-buildpack-nodejs
        ````

    3. For other languages and frameworks

        ````
        https://github.com/michrome/heroku-buildpack-mozjpeg-encoder
        # See https://devcenter.heroku.com/articles/buildpacks#default-buildpacks for your language/framework
        ````

## Examples apps using heroku-buildpack-mozjpeg-encoder

1. [Node.js](https://github.com/michrome/heroku-buildpack-mozjpeg-encoder-example-node)
