# lagoon-gatsby
An approach to incremental builds for Gatsby in Lagoon

## Prerequisites
This package is designed to be used inside Lagoon, so of course you need a lagoon project! In the Lagoon project, you'll need a container that is able to run the `lagoon-gatsby` executable from this repository. 

The `lagoon-gatsby` binary requires rsync to be installed in your container.

## Installation
TODO

## Usage

### Incremental build
LAGOON_GATSBY_APP=/app LAGOON_GATSBY_STORAGE=/app/storage/ /app/lagoon-gatsby build incremental

### Clean build
LAGOON_GATSBY_APP=/app LAGOON_GATSBY_STORAGE=/app/storage/ /app/lagoon-gatsby build clean
