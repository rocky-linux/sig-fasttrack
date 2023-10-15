# SIG/Fasttrack Wiki

  FastTrack, as an ode to a past CentOS repository of a similar name, is a SIG to attempt to provide the following:

  * Fixes, customizations, improvements to packages that the community would like to see
  * This also includes doing backports of patches that may not be released by our upstreams to address any type of bugs
  * Potential packages that could potentially make it to CentOS Stream or EPEL
  * Newer versions of software that override the base repositories that would likely never land in RHEL, CentOS Stream, or EPEL

## Continuous Integration / Continuous Deployment

Actions Runner executes workflow to publish to https://sig-fasttrack.rocky.page on push to main.

## Local testing

A Dockerfile and docker-compose are included for local testing.  "docker-compose up"  (or "podman-compose up") should be enough to launch this wiki locally.  Point your browser to http://localhost:8000 to view.
