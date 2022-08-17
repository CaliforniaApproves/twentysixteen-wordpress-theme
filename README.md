# California Approves Twenty Sixteen Theme

This repository contains the customized version of the Twenty Sixteen Wordpress
theme used by [californiaapproves.org](https://californiaapproves.org).

## Development

### How to deploy

We deploy by pushing to a git repository on the webserver.

Pre-requisites:

1. Clone this repository locally
1. SSH Access to californiaapproves.org
1. Add production and staging repositories
   - `git remote add production califrl1@162.241.217.183:public_html/wp-content/themes/twentysixteen`
   - `git remote add staging califrl1@162.241.217.183:public_html/staging/6769/wp-content/themes/twentysixteen`

Deploying

1. `git checkout master`
1. `git push production master`
1. `git push staging master`

## Hosting

The website is hosted with BlueHost behind a Cloudflare Basic cache.

- Assets are cached for 1 week and pages for 5 minutes.
- Cloudflare minifies and compresses the pages

## Domain Registration

We have the following domains:

- californiaapproves.org registered with NameCheap
- calapproves.org is registered with wordpress.com until Feb 2023. It is
configured to point to a vultr.com server (207.148.13.93) that redirects to
californiaapproves.org because wordpress.com wants to charge for redirection.

## DNS Configuration

DNS is provided by Cloudflare with these servers configured in NameCheap:

- aldo.ns.cloudflare.com
- ariella.ns.cloudflare.com

## HTTPS/SSL Configuration

Bluehost provides the SSL certificates for californiaapproves.org

LetsEncrypt provides the SSL certificates for calapproves.org. This is managed
on the Vultr server with certbot.
