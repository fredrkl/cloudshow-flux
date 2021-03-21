# cloudshow-flux
This repo shows how you can use [Flux](https://fluxcd.io/) to describe your entire system as code, and do rapid changes to it for throubleshooting.

## Bootstrap
Make sure you have sealed secrets controller running if you plan on having sealed secrets as part of your repos. This demo also presumes that you have Linkerd installed with the viz add-on.

### Install Flux CLI
Install the Flux CLI from https://toolkit.fluxcd.io/get-started/#install-the-flux-cli.

### Bootstrap
Run the following command

```
> flux install
> flux create source git root \
  --url=https://github.com/fredrkl/cloudshow-flux  \
  --branch=main
> flux create kustomization root \
  source=root
```