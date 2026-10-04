# EuroHPC JU HPC-QC and quantum devices access in practice

An ENCCS lesson on EuroHPC quantum access as it works in practice: applying, onboarding at each
hosting site, and getting a circuit onto each of three machines (Euro-Q-Exa at LRZ, Piast-Q at PCSS,
VLQ at IT4Innovations). It is the long form of the ENCCS blog post of the same title.

Published address: https://enccs.github.io/eurohpc-quantum-devices-access-hpcqc/ Repository: https://github.com/ENCCS/eurohpc-quantum-devices-access-hpcqc

## Quick commands

Run these one level above this directory, from the root of the repository that holds it.

```console
# build the lesson and open it
pixi run -e docs lesson && open lesson/_build/html/index.html

# open one page after a build, for example the HPC-QC page
open lesson/_build/html/hpc-qc.html

# start from a clean build
rm -rf lesson/_build && pixi run -e docs lesson

# edit the pages
zed lesson/content

# rebuild the two figures after editing blog/figs/*.mmd, then copy them in
./blog/figs/rebuild.sh && cp blog/figs/*.drawio.png lesson/content/_static/

```

The build treats warnings as errors, so a broken link or a bad directive stops it and says where.

## What this directory is

An instance of [ENCCS/sphinx-lesson-template](https://github.com/ENCCS/sphinx-lesson-template),
branch `cc3-footer`, commit `2efcd6e`. The tree is the template's tree, so the directory can be
lifted out as a repository of its own. The template's own `README.md` is empty at that commit, so
this file is written for this lesson.

Taken from the template unchanged: `.github/workflows/sphinx.yml`, `.gitignore`, `LICENSE`,
`LICENSE.code`, `Makefile`, `make.bat`, `pylock.toml`, `requirements.txt`,
`content/_templates/page.html`, and everything the template has in `content/_static/` (the
stylesheet, the logos, the favicon). The EuroCC 3 disclaimer in the footer is the `copyright` string
in `content/conf.py`, and the partner logos come from `content/_templates/page.html`. Neither is
reworded here, and the pages do not repeat them.

Changed for this lesson: `content/conf.py` (title, author, repository name, year, and one filter for
a warning, each marked with a comment), `pyproject.toml` (name and description), `CITATION.cff`
(title and author), and the pages in `content/`. Added: the two figures in `content/_static/`.

`pylock.toml` is the template's file as exported there. It has not been regenerated for this lesson
and still names the template as the project; regenerate it once the lesson has its own repository.

## Layout

| Path | What it holds |
|---|---|
| `content/index.md` | Front page: prerequisites, the lesson map, learning outcomes, acknowledgement, licence |
| `content/access.md`, `onboarding.md` | Getting access, and onboarding at each site |
| `content/machines.md` | How the three machines differ |
| `content/hpc-qc.md` | HPC and HPC-QC: the machines at supercomputing centres, reaching LRZ's HPC-QC system, further reading |
| `content/euro-q-exa.md`, `vlq.md`, `piast-q.md` | One page per machine |
| `content/qpu-hours.md` | How time is metered |
| `content/quick-reference.md` | Quick reference |
| `content/_static/*.drawio.png` | The two figures, copied from the blog post's figures |

## Build

The lesson builds with pixi from the root of the repository that holds this directory:

```console
$ pixi run -e docs lesson
```

That runs `sphinx-build -n -W --keep-going -b html lesson/content lesson/_build/html`: nitpicky,
warnings as errors, into `lesson/_build/`, which is the build directory the template's `Makefile`
and `.gitignore` expect. The `docs` environment is defined in the root `pyproject.toml` and holds
the six dependencies this directory's own `pyproject.toml` declares, on Python 3.13. The build
executes no code and contacts no machine.

Once this directory is a repository of its own, the template's `Makefile` and its GitHub workflow
apply as they are.

## To decide before publication

- **Timings.** The template's front-page table gives minutes per page. This lesson has not been
  taught, so the table lists what each page covers instead. Add the minutes after the first run.
- **The year.** `content/conf.py` and the licence block say 2026 where the template says 2025.
  `LICENSE.code` is the template's file and is left as it is.
- **A privacy read** of the Markdown and of the rendered HTML: no usernames, personal paths, tokens,
  keys or scheduler logs, and no project identifiers other than those in the acknowledgement.

## The rule for editing

The blog post is edited first and the lesson follows. The
sentences here about how each site works and how each site meters time are the post's sentences,
reused with every hedge, and they were reviewed there. Do not improve them here. If one has to
change, change it in the post, have it reviewed, and then carry it over.

Two further rules follow from the post:

- The three site acknowledgement wordings on the front page are reproduced as the sites supplied
  them, including the missing full stops. Do not edit them.
