# gds-development-scripts

Some useful scripts for development at GDS.

## Installation

Clone the project into your VM. These scripts should always be run inside your
vm.

```bash
cd /var/govuk
git clone https://github.com/AndrewVos/gds-development-scripts
```

## Health check

This script checks the health of your various projects. All projects
are assumed to be located in `/var/govuk`.

Common problems that people are checked:

### Mongo

Ensures that mongodb is running, and launches it if it is not.

### Git

Ensures repositories are up to date. Will only pull the repository if it
is on the `master` branch.

### Gems

Ensures that bundle install has been run, if the project has a `Gemfile`.

### DB

Ensures that `rake db:create` and `rake db:migrate` have been run.

## Usage

Always run this script from `/var/govuk` (inside your VM).

If the `gds` script has been added to your path:

```bash
cd /var/govuk
# run a health check
gds --health
```

If the gds script hasn't been added to your path:

```bash
cd /var/govuk
./gds-development-scripts/gds --health
```
