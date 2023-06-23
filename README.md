# op
# author: @MikeRalphson
# issue: various

#
# This workflow creates the agenda issue each week. It runs on a cron every
# Monday morning, raising an issue for the following Thursday.
# It can also be run manually, in case GitHub Actions has a failure.
#

on:
  schedule:
    - cron: '0 16 * * 4'
  workflow_dispatch: {}
  
jobs:
  agenda:
    env:
      GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

    runs-on: ubuntu-latest
