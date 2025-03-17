# pnpm-dlx-manifest
Demonstration of pnpm 10.6.1 attempting to read project manifest on dlx command

https://github.com/pnpm/pnpm/issues/9263

# To test

Run the following commands.  Only the `10.6.1-with-allow-build` should error:

```
docker run $(docker build -q --file Dockerfile-10.5.2-with-allow-build .)
docker run $(docker build -q --file Dockerfile-10.6.1-with-allow-build .)
docker run $(docker build -q --file Dockerfile-10.6.1-without-allow-build .)
```
