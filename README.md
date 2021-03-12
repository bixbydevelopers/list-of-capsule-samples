# List of Capsule Samples

There are many capsule samples that can be used to learn how to write a new capsule for Bixby.
This repository is meant to grow into a list/index of them all.

This repository is a work in progress. We're collecting together a list of the capsule sample repositories here,
that includes descriptions, name of their GitHub repositories, and screenshots. More information will be available
here as this develops.

# JSON format

The `samples.json` file describes all capsule samples in a list. Each element of the array in this list
includes the following information about the capsule sample that it describes:
* name: capsule name for display (e.g. "Movie Agent")
* id: capsule id in the capsule.bxb file (e.g. "example.bank")
* group: capsule grouping or author or type, for display (e.g. "Walkthrough" or "Sample")
* github.owner: name of the GitHub org that owns the capsule repo (e.g. "bixbydevelopers")
* github.repo: name of the GitHub repo that contains the capsule (e.g. "capsule-sample-movie-agent")
* github.folder: relative path to a sub-folder, in that GitHub repo, if the capsule is part of a collection (e.g. "input-form")
* links: array of links to the docs for the feature or walk-through that this capsule exhibits
* screenshots: array of screenshots to show for this capsule, these are relatives paths to the files from the top of this repo
* highlightScreenshotIndex: screenshot that should show in the list (if there are multiple screenshots, index begins at 0)
* description: description of walk-through or feature that is highlighted by this sample
* focusPath: relative path from capsule top-level, to the file that the developer should look at first (e.g. "README.md")
