# brownfield land collection

[![License](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/digital-land/brownfield-land/blob/master/LICENSE)

A collection of individual [brownfield land registers](https://www.gov.uk/guidance/brownfield-land-registers) collected each night from local planning authorities, which are processed and then assembled into a national dataset.

The national dataset is in a format consistent with other Digital Land datasets as defined by the [brownfield-land schema](https://digital-land.github.io/specification/schema/brownfield-land/).

* [brownfield land registers](https://www.gov.uk/guidance/brownfield-land-registers) — GOV.UK guidance for local planning authorities on brownfield land to be included in their register.
* [publish your brownfield land data](https://www.gov.uk/government/publications/brownfield-land-registers-data-standard/publish-your-brownfield-land-data) — guidance for local planning authorities on the data format when publishing brownfield land data.

# Collection

* [collection/source.csv](collection/source.csv) — the list of data sources by organisation, see [specification/source](https://digital-land.github.io/specification/schema/source/)
* [collection/endpoint.csv](collection/endpoint.csv) — the list of endpoint URLs for the collection, see [specification/endpoint](https://digital-land.github.io/specification/schema/endpoint)
* [collection/resource/](collection/resource/) — collected resources
* [collection/log/](collection/log/) — individual log JSON files, created by the colletion process
* [collection/resource.csv](collection/resource.csv) — an index of collected resources, see [specification/resource](https://digital-land.github.io/specification/schema/resource)

# Rebuilding the collection

We recommend working in [virtual environment](http://docs.python-guide.org/en/latest/dev/virtualenvs/) before installing the python [requirements](requirements.txt), [makerules](https://github.com/digital-land/makerules) and other dependencies:

    $ make makerules
    $ make init
    $ make collect

# Building the national dataset

Collected files can be converted into a national dataset:

    $ make

# Nightly collection

The collection is [updated nightly](https://github.com/digital-land/brownfield-land-collection/actions) by the [GitHub Action](.github/workflows/run.yml).

# Licence

The software in this project is open source and covered by the [LICENSE](LICENSE) file.

Individual datasets copied into this repository may have specific copyright and licensing, otherwise all content and data in this repository is
[© Crown copyright](http://www.nationalarchives.gov.uk/information-management/re-using-public-sector-information/copyright-and-re-use/crown-copyright/)
and available under the terms of the [Open Government 3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/) licence.
