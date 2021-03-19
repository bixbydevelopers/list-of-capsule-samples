# List of Capsule Samples

There are many capsule samples that can be used to learn how to write a new capsule for Bixby.
This repository is meant to grow into a list/index of them all.

This repository is a work in progress. We're collecting together a list of the capsule sample repositories here,
that includes descriptions, name of their GitHub repositories, and screenshots. More information will be available
here as this develops.

# JSON format

The `samples.json` file contains the list of sample capsules. The top-level properties in this file describe the
list itself, and includes an array that contains objects that describe each of the sample capsules:

- title: what to display at the top of the list (e.g. "Select a Capsule")
- description: what to display under the title, in an array strings, one for each paragraph
- links: an array of links to the documentation about sample capsules and walkthroughs, each link object contain "text" and "url" properties
- samples: an array of sample capsule description objects (described below)

Each sample capsule in the `samples` array has these properties:

- name: capsule name for display (e.g. "Movie Agent")
- id: capsule id for the `capsule.bxb` file (e.g. "example.movieAgent")
- group: capsule grouping, author or type, for display (e.g. "Walkthrough" or "Sample")
- github.owner: name of the GitHub organization that owns the capsule repo (e.g. "bixbydevelopers")
- github.repo: name of the GitHub repo that contains the capsule (e.g. "capsule-sample-movie-agent")
- github.folder: relative path to a sub-folder in the GitHub repo, if the capsule is part of a collection (e.g. "input-form")
- links: array of links to the docs for the feature or walk-through that this capsule exhibits, each link object contain "text" and "url" properties
- screenshots: array of URLs for the screenshots to show for this capsule
- highlightScreenshotIndex: screenshot that should show in the list (if there are multiple screenshots, index begins at 0)
- description: description of walk-through or feature that is highlighted by this sample, an array of strings, each string will be displayed as a paragraph
- focusPath: relative path from the capsule's top-level folder, to the file that the developer should look at first (e.g. "README.md")
