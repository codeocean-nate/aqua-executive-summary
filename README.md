# executive-summary (Aqua skill)

An Aqua skill that ends every reply over 3000 characters with an `## Executive Summary` section: 3 to 5
bullets, at most 1500 characters, covering the findings, the numbers that carry them, and the next step.
Shorter replies are left exactly as written. The skill itself is [SKILL.md](SKILL.md).

## Install on a Code Ocean deployment

Create a skill cloned from this repository, so it stays linked: in an Aqua chat, ask
"Create a skill in my Skills cloned from https://github.com/codeocean-nate/aqua-executive-summary",
or create a new skill from this Git repository in the Skills page. The deployment needs github.com
egress, and a private copy of this repo needs a GitHub credential under Account > Credentials that can read it.

## Updating

Edit SKILL.md here and push. A linked skill shows the new commit as a pull on its Timeline; Sync with
GitHub brings it in. Edits made in Code Ocean push back the same way.
