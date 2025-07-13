# Conditional GitHub CI That Must Pass If Run

This is a test repo to demonstrate how you can set up checks that *must pass* if they run, but *do not have to run*.

View this repo's pull requests to see one that passes (because its conditional checks pass) and one that fails (because its conditional checks fail).

Basic GitHub workflows/actions/jobs do not support this in any configuration. But the merge-gatekeeper action plugs that gap. 

You set merge-gatekeeper as the job that must pass in a branch ruleset and it monitors all other checks on the PR and reports success only if they all pass. If it fails merging will be blocked.

There is no way to have a check that runs but does not need to pass under this system, but I see that as a feature.

The GitHub branch ruleset (under Settings, Rules) that make this work:

<img width="1258" height="1336" alt="image" src="https://github.com/user-attachments/assets/56969748-09c9-4ea4-a187-a6e0200eb399" />

