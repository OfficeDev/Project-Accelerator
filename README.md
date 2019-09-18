---
page_type: sample
products:
  - office-project
description: An Issues model that integrates with Project on CDS
urlFragment: update-this-to-unique-url-stub
languages:
  - powerapps
---

# Issues Model for Project on Dynamics

Project stores data in the Common Data service. Now, developing apps that extend Microsoft Project is easier than it has ever been before.

This repository contains an [unmanaged solution](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/introduction-solutions) with an Issues model. You are encouraged to edit it, reuse it, and provide feedback about it. Depending upon the kinds of changes you suggest, I will incorporate them into the model. There are two goals for the content in this repository.

**Primary goal:** Give an example for how you can extend Project and package a solution.

**Aspirational goal:** Iterate on a simple base to develop a best-in-class Issues model that can be reused and repurposed for other scenarios.

*NOTE: The content in this repo is not part of a supported release of Microsoft software; it is managed by me. However, I will reply to issues and integrate pull requests when I think they help to further the two goals of this repository.*

## Contents of this Repository

What you'll find in this repository.

| File/folder           | Description                                |
|-----------------------|--------------------------------------------|
| `.gitignore`          | Define what to ignore at commit time.      |
| `CONTRIBUTING.md`     | Guidelines for contributing to the sample. |
| `CHANGELOG.md`        | List of changes to the sample.             |
| `README.md`           | This README file.                          |
| `LICENSE`             | The license for the sample.                |
| `Issues <version>.zip`| The Issues solution                        |

## Contents of the `Issues` solution

The contents right now are pretty basic.

1. The Issues entity
1. Relationships between Tasks and Projects

The list of contents will expand based on your feedback and any code contributions you make 😊.

## Prerequisites

You'll need a few things to deploy this solution.

1. A license to Project Pro or Project Premium
1. A Dynamics org with the new Project solution deployed to it.
1. Permissions to deploy solutions in the Default Dynamics org.
1. If you are also planning on developing Power Apps using this solution, you'll also need a Power Apps license.

## Deploying the solution

There are a few different ways that you can deploy a solution on Dynamics. You can learn more about them [here](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/introduction-solutions). The one that I'll focus on is deploying via [powerapps.com](https://powerapps.com). 

1. Download the `Issues <version>.zip` from this repo.
1. Sign into [powerapps.com](https://powerapps.com).
1. In the top header, in the "environment" section, select the Default environment (This is where we deployed the new Project Service).
1. On the left navigation, click the "solutions" link.
1. You should see a list of the solutions in the default org. Now click on the "Import" button along the top nav of this page
1. In the popup, press the "choose file" button and navigate to the local directory where you downloaded the `Issues <version>.zip` file.
1. Press the "next" button and then "import" to begin importing the solution. This will take a few minutes.
1. Once that is done, you'll be able to close the pop-up, and you should now see the "Issues" solution in the list of solutions. If you don't see the Issues solution, ensure that "all" solutions are shown, by clicking on the filter button on the top-right of the list of solutions.

## Contributing

I welcome changes that include new entities, relationships, views, fields on existing entities, etc. If you contribute, please share your contributions as unmanaged solutions so that I can integrate them.

Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have
the right to, and actually do, grant us the rights to use your contribution. For
details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether
you need to provide a CLA and decorate the PR appropriately (e.g., status check,
comment). Simply follow the instructions provided by the bot. You will only need
to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of
Conduct](https://opensource.microsoft.com/codeofconduct/). For more information
see the [Code of Conduct
FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact
<opencode@microsoft.com> with any additional questions or comments.
