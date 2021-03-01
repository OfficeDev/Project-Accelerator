---
page_type: sample
products:
  - office-project
description: An Issues model that integrates with Project on CDS
languages:
  - powerapps
---

# Project for the web Accelerator

_NOTE: The content in this site is not a supported release of Microsoft software._

The Project for the web Accelerator is applies useful customizations to the Project for the web Power App. The Accelerator can _easily_ be deployed to any environment that has Project for the web already in it. Scenarios included in the Accelerator are...

💡 **Project Requests**. Create a list of ideas for Projects that include a business case and expected impact. Pro-tip: Create an Approvals flow using Power Automate to convert Project Requests into Projects.

💼 **Programs**. Create a heirarchy of programs and projects see how work fits into the bigger picture.

🔥 **Risks and Issues**. Manage the surprises that accompany every project. Create and assign risks and issues to minimize impacts to a project's schedule.

🚧 **Changes**. Use change tracking processes to help understand the history of a project.

📝 **Status**. Centralize recording of project status to keep stakeholders up-to-date.

The Project Accelerator is completely customizable. If something is missing: add it! Sign into [PowerApps](https://make.powerapps.com) to make additional customizations to the Project Power App.

This repository also contains a Power BI template that can be deployed alongside the Accelerator. For the best experience, deploy the Accelerator, deploy the Power BI content pack, and then customize the Accelerator to use the deployed Power BI content pack. **Follow the instructions below to get started!**

## Contents of this GitHub Repository

| File                                                 | Description                                              |
| ---------------------------------------------------- | -------------------------------------------------------- |
| `README.md`                                          | This README file.                                        |
| `Project for the web Accelerator Full <version>.zip` | Accelerator *without* Programs and Business Case       |
| `Project for the web Accelerator Full <version>.zip` | Accelerator that includes Programs and Business Case |
| `Project for the web template.pbit`                  | Power BI template for use with the Accelerator |

_NOTE: The program management and business case scenarios are impacted by a critical bug in Project for the web. Until that bug is fixed, projects cannot be parented to programs and projects cannot be given business cases. We are working on a fix that will be available soon. Until then, deploy the Lite version of the Accelerator to remove those scenarios._

## Deploying the solution

### Prerequisites

* An environment with the Project Solution in it. [Learn more about deploying Project](https://docs.microsoft.com/project-for-the-web/deploying-project).
*  Admin rights to the environment
*   Rights to create Power Automate flows using the Common Data Service connector.
*   A local copy of either the [Full](Project%20for%20the%20web%20Accelerator%20Full%20v1_6_0_12.zip) or [Lite](Project%20for%20the%20web%20Accelerator%20Lite_v1_6_0_11.zip) version of the Accelerator. You don't need to unzip the solution file.

### Instructions

1. Sign into [powerapps.com](https://make.powerapps.com).
2. In the top header, open the *Environment* menu and select the environment you have the Project solution installed in.
3. On the left navigation, click the *Solutions* menu item.
4. Click on the *Import* button in the top menu bar of this page.
5. In the popup, press the *choose file* button and navigate to the local directory where you downloaded the `Accelerator` zip file.
6. Press *next*, and select an existing connection to a Power Automate flow or create a new one.
7. Press the *next* button and then *import* to begin importing the solution. This will take several minutes, so grab a coffee ☕.

**Once this has been completed you're done deploying the solution!**

The Project Power App in this environment will look similar to the screenshot below. If you want to make a change, you can deploy a managed solution with additional changes, or edit the Project Power App yourself in [PowerApps.com](https://make.powerapps.com).

 ![Project Power App with Accelerator](project-with-the-accelerator.png)

## Deploying the Power BI template

### Prerequisites

* An environment with Project for the web and the Project Accelerator in it.
* The appropriate privileges to deploy the Power BI content pack to powerbi.com.
* Admin rights to modify the Project Power App so that you can add the content pack to it.

### Instructions to deploy the Power BI template
1. Download the [Power BI template](Project%20for%20the%20Web%20Accelerator%20report.pbit) for the Accelerator.
2. Deploy it using Power BI Desktop or in the [PowerBI.com service](https://www.powerbi.com).
3. When prompted for the environment url, use the base url of your environment. For example: `https://myenvironment.crm.dynamics.com`

### Instructions to modify the Project Accelerator to use the deployed template
The Accelerator already contains a placeholder for the Power BI template. Once you've deployed the Accelerator and the Power BI template, follow these steps to have the Power BI report appear in the Accelerator.

1. Sign into [powerapps.com](https://make.powerapps.com).
2. In the top header, open the *Environment* menu and select the environment you have the Project solution installed in.
3. On the left navigation, click the *Solutions* menu item.
4. Click the *Project for the web Accelerator* solution name to open the solution.
5. Click the *Reports* item. It has the name *proj_Reports* and is of type *Customization.Type_WebResource*.
6. 

## License Requirements

The Accelerator solution and Power BI template are distributed free of charge under the MIT license.
However, using them in your environments to work with *Project for the web* has certain licensing implications.

### Using the Accelerator without the Power BI content pack (INCOMPLETE)

If you just deploy the Accelerator without the Power BI content pack, users will need the following licenses.

Making full use of all the customizations requires a Project Plan 3 license. This applies to your project managers who also need to do things like organize programs, track issues and risks, manage the business case and financials, or edit the custom columns such as corporate sponsor of the project.

Users who are only creating and managing tasks need a Project Plan 1 license.

Refer to the [Project Service Description](https://docs.microsoft.com/office365/servicedescriptions/project-online-service-description/project-online-service-description) for details about Project licensing.

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
