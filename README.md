# lagoon-gatsby
An approach to incremental builds for Gatsby in Lagoon

## Prerequisites
This package is designed to be used inside Lagoon, so of course you need a lagoon project! In the Lagoon project, you'll need a container that is able to run the `lagoon-gatsby` executable from this repository. 

The `lagoon-gatsby` binary requires rsync to be installed in your container.

## Installation
TODO

## Usage
You can set `LAGOON_GATSBY_APP` and `LAGOON_GATSBY_STORAGE` in your docker image build, in Lagoon, or on the command line

`LAGOON_GATSBY_APP`: Generally where you Gatsby app lives (usually /app for Lagoon projects)

`LAGOON_GATSBY_STORAGE`: Persistent storage mounted by Lagoon. If this isn't persistent, incremental builds are impossible

### Incremental build
RUN: `LAGOON_GATSBY_APP=/app LAGOON_GATSBY_STORAGE=/app/storage/ /app/lagoon-gatsby build incremental`

### Clean build
RUN: `LAGOON_GATSBY_APP=/app LAGOON_GATSBY_STORAGE=/app/storage/ /app/lagoon-gatsby build clean`
