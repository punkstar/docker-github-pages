# Docker Image for GitHub Pages

This image provides an environment for previewing Jekyll sites in a GitHub pages environment on your local machine.

## Usage

Create a script called `run.sh` in your project with the following contents:

    docker run --rm \
      -v $(pwd):/site \
      -p 4000:4000 \
      punkstar/github-pages \
      serve --watch --incremental --port 4000 --host 0.0.0.0

Your site will now be available at http://localhost:4000, or whatever IP you're running Docker on.
