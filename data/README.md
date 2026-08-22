# Team bundles

One folder per team under `teams/<slug>/`, each a self-contained bundle:

    teams/colombia/
      team.json      name, colours, formation, squad
      logo.png       the crest
      flag.png       the national flag (120x80)
      kit_01.png     home kit
      kit_02.png     away kit

This is the source the game compiles from. The generated database and the
packed art that ship inside the game are NOT here - a maintainer regenerates
them from these bundles at release time. To add a team, add a folder here
(the GoalKick Editor writes one for you) and open a pull request. See the
top-level README for the full guide and the art/legal rules.
