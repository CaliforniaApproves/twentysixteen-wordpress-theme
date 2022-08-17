# California Approves Twenty Sixteen Theme

This repository contains the customized version of the Twenty Sixteen Wordpress
theme used by [californiaapproves.org](https://californiaapproves.org).

## Development

### Deployment

We deploy by pushing to a bare git repository on the webserver.

Pre-requisites:

1. Clone this repository locally
1. SSH Access to californiaapproves.org
1. Add production and staging repositories
   - `git remote add production califrl1@162.241.217.183:public_html/wp-content/themes/twentysixteen`
   - `git remote add staging califrl1@162.241.217.183:public_html/staging/6769/wp-content/themes/twentysixteen`

Pushing:

1. `git checkout master`
1. `git push production master`
1. `git push staging master`
