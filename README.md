# List of Capsule Samples

There are many [sample capsules](https://bixbydevelopers.com/dev/docs/sample-capsules) that can be used to learn how
to write a new capsule for Bixby. This repository is the index. We've collected together information about all the
sample capsules here, and it includes descriptions, names of their GitHub repositories, and screenshots.

This repository provides the list of sample capsules that is featured in Bixby Studio, beginning in
[version 8.10](https://bixbydevelopers.com/dev/docs/dev-guide/release-notes/bixby-studio.8-10-0#download-and-open-sample-capsules).
To get started, choose "Create Capsule from Sample" from the File Menu, or from the Welcome page.
Bixby Studio will show you the list of sample capsules and, once you select one, it will download a copy of that
sample capsule into a local folder of your choice and open it for you.

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
- github.branch: name of the GitHub branch that contains the capsule (assumed to be "main", if not specified)  
- github.folder: relative path to a sub-folder in the GitHub repo, if the capsule is part of a collection (e.g. "input-form")
- links: array of links to the docs for the feature or walk-through that this capsule exhibits, each link object contain "text" and "url" properties
- screenshots: array of URLs for the screenshots to show for this capsule
- highlightScreenshotIndex: screenshot that should show in the list (if there are multiple screenshots, index begins at 0)
- description: description of walk-through or feature that is highlighted by this sample, an array of strings, each string will be displayed as a paragraph
- focusPath: relative path from the capsule's top-level folder, to the file that the developer should look at first (e.g. "README.md")

# Updating this list

This list is meant to be updated by the Bixby team, and instructions for doing so can be found in the
[Sample Capsule List Guide](https://github.com/six5/viv-ide/blob/master/notes/sample-capsule-list-guide.md)
(this link leads to a private repository that not everyone will be able to open). 

Care should be taken when updating the `samples.json` file, because any updates to that file on the main branch of
this repository will immediately be reflected in all installed copies of Bixby Studio (version 8.10 or greater).
Bixby Studio loads the `samples.json` file from this repository to display the list of sample capsules available.
