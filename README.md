# docker-simplytranslate-quay

A [SimplyTranslate](https://codeberg.org/SimpleWeb/SimplyTranslate-Web) image, on Quay.

[Quay page](https://quay.io/repository/pussthecatorg/simplytranslate) | [GitHub page](https://github.com/PussTheCat-org/docker-simplytranslate-quay)

This image mostly exist for the [PussTheCat.org](https://pussthecat.org/) [instance](https://simplytranslate.pussthecat.org/), but others are free to use it.

## Usage:

- Download (or copy the content of) the `docker-compose.yml` 
- Download (or copy the content of) the `config.conf` from this repository, or from upstream: https://codeberg.org/SimpleWeb/SimplyTranslate-Web/src/branch/master/config.conf.template
- Customize the `config.conf` file how you want
- Move both files to the folder you want
- `docker-compose up -d`

## Credit:

- The Invidious `container-release.yml` file: https://github.com/iv-org/invidious/blob/master/.github/workflows/container-release.yml
- [@unixfox](https://github.com/unixfox), invidious-custom `docker-image.yml` file: https://github.com/unixfox/invidious-custom/blob/master/.github/workflows/docker-image.yml
