G0cr / g0vcaptcha
=================

## Dev
---

* perl (>= 5.14)
* ElasticSearch
* tesseract
* ImageMagick
* GNU parallel

### Mac Homebrew:

    brew install elasticsearch
    brew install tesseract --all-languages
    brew install imagemagick
    brew install parallel

### perl stack setup

Setup perlbrew

    \curl -L http://install.perlbrew.pl | bash
    perlbrew install perl-5.20.0 --as project-g0cr --notest
    perlbrew use project-g0cr
    perlbrew install-cpanm

Deal with CPAN dependencies

    cpanm --notest Carton
    carton install

Initialize ElasticSearch index.

    elasticsearch --config=/usr/local/opt/elasticsearch/config/elasticsearch.yml -d
    carton exec script/prepare-elasticsearch

Running the mojo webapp:

    carton exec morbo ./script/g0cr

Running the background process webapp:

    carton exec morbo ./script/process-document

## Data Model

- doc
  - id
  - filename
  - created_at

- page
  - id
  - doc_id
  - created_at

- bbox
  - id
  - page_id
  - location_top
  - location_left
  - location_bottom
  - location_right
  - created_at

- recognition
  - id
  - bbox_id
  - created_at
  - content

- recognition_confirmation
  - id
  - recognition_id
  - created_at

