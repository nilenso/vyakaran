# Branching

## distributed version control is an immutable database

* branch based development
* see [https://trunkbaseddevelopment.com/](https://trunkbaseddevelopment.com/)
* Try both, but only use one per project.

## horror story: unsync'd, un-roll-backable commit

* time
* sync
* rollback \(health, safety\)
* API =&gt; schema =&gt; data \(implicit schema\) =&gt; behaviour \(implicit data\)
* commit to master
* deployment
* migration
* testing
* communication

## doing it right: What is the reverse of each of the above?

## squash and merge

* history is lost
* contributor contributions are lost because whoever merges it gets puts up as the author and the commits get aggregated into a single commit
* running stratified pull requests becomes hard because squashing aggregates history and now your dependent PR has commits that don't exist and show up as new changes
* weakens the enforcement on writing high quality commit messages per commit
* the argument for it is typically for aesthetic reasons: "clean history" -- this can be simply achieved by looking at the tags that were deployed which would have summarized milestones for what went in for each release

