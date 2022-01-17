# simplytranslate-quay

A [simplytranslate](https://sr.ht/~metalune/SimplyTranslate/) image, on Quay.

https://quay.io/repository/pussthecatorg/simplytranslate

This image mostly exist for the [PussTheCat.org](https://pussthecat.org/) [instance](https://simplytranslate.pussthecat.org/), but others are free to use it.

## Usage:

- Download (or copy the content of) the `docker-compose.yml` 
- Download (or copy the content of) the `config.conf` from this repository, or from upstream: https://git.sr.ht/~metalune/simplytranslate_web/tree/master/item/config.conf
- Customize the `config.conf` file how you want
- Move both files to the folder you want
- `docker-compose up -d`

## Credit:

- The Invidious `container-release.yml` file: https://github.com/iv-org/invidious/blob/master/.github/workflows/container-release.yml
- [@unixfox](https://github.com/unixfox), invidious-custom `docker-image.yml` file: https://github.com/unixfox/invidious-custom/blob/master/.github/workflows/docker-image.yml
