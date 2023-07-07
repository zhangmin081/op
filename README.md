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
node_modules
.env
coverage
coverage.json
typechain
typechain-types
docs/console.md
/
.env
coverage
coverage.json
typechain
typechain-types
We have made progress on "EIP-4844: Shard Blob Transactions" (#27257, #27256, #27155, #27049), beacon light sync (#27292), and path-based state storage (#27176, #26813) but neither is finished as of yet.
