---
page_type: sample
products:
  - office-project
description: An Accelerator solution for Project for the web
languages:
  - powerapps
  - Power BI
---

# Project for the web Accelerator

The Project for the web Accelerator applies useful customizations to the Project for the web Power App. The Accelerator can _easily_ be deployed to any environment that has Project for the web already in it. Scenarios included in the Accelerator are...

💡 **Project Requests**. Create a list of ideas for Projects that include a business case and expected impact. Pro-tip: Create an Approvals flow using Power Automate to convert Project Requests into Projects.

💼 **Programs**. Create a heirarchy of programs and projects see how work fits into the bigger picture.

🔥 **Risks and Issues**. Manage the surprises that accompany every project. Create and assign risks and issues to minimize impacts to a project's schedule.

🚧 **Changes**. Use change tracking processes to help understand the history of a project.

📝 **Status**. Centralize recording of project status to keep stakeholders up-to-date.

This repository also contains a Power BI template that can be deployed alongside the Accelerator. For the best experience, deploy the Accelerator, then deploy the Power BI content pack, and finally, customize the Accelerator to use the deployed Power BI report. **Follow the instructions below to get started!**

---

### [Here's the latest version of the Accelerator](https://github.com/OfficeDev/Project-Accelerator/blob/main/releases/Project_for_the_web_Accelerator_v1_7_0_3.zip?raw=true)
### [Here's the latest version of the Power BI Template for the Accelerator](https://github.com/OfficeDev/Project-Accelerator/blob/main/releases/Project_for_the_Web_Accelerator_report.pbit?raw=true)

---

## Contents of this GitHub Repository

| File                                            | Description                                                                                                 |
| ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `README.md`                                     | This README file.                                                                                           |
| `LICENSE.md`                                    | Details about the MIT License for anyone looking to reuse code in this repository in their own applications |
| `releases`                                      | folder containing the Project for the web Accelerator                                                       |
| `Project for the web template.pbit`             | Power BI template for use with the Accelerator                                                              |

---

## Deploying the solution

### Prerequisites

- An environment with the Project for the web solution in it. [Learn more about deploying Project](https://docs.microsoft.com/project-for-the-web/deploying-project).
- Admin rights to the environment
- Rights to create Power Automate flows using the Common Data Service connector.

- A local copy of the [Accelerator](https://github.com/OfficeDev/Project-Accelerator/blob/main/releases/Project_for_the_web_Accelerator_v1_7_0_3.zip?raw=true). You don't need to unzip the solution file.

### Instructions

1. Sign into [powerapps.com](https://make.powerapps.com).
2. In the top header, open the _Environment_ menu and select the environment you have the Project solution installed in.
3. On the left navigation, click the _Solutions_ menu item.
4. Click on the _Import_ button in the top menu bar of this page.
5. In the popup, press the _choose file_ button and navigate to the local directory where you downloaded the `Accelerator` zip file.
6. Press _next_, and select an existing connection to a Power Automate flow or create a new one.
7. Press the _next_ button and then _import_ to begin importing the solution. This will take several minutes, so grab a coffee ☕.

**Once this has been completed you're done deploying the solution!**

The Project Power App in this environment will look similar to the screenshot below. If you want to make a change, you can deploy a managed solution with additional changes, or edit the Project Power App yourself in [PowerApps.com](https://make.powerapps.com).

![Project Power App with Accelerator](images/project-with-the-accelerator.png)

## Deploying the Power BI template

### Prerequisites

- An environment with Project for the web and the Project Accelerator in it.
- Admin rights to the environment
- The appropriate privileges to deploy the Power BI content pack to powerbi.com.

### Instructions to deploy the Power BI template

1. Download the [Power BI template](https://github.com/OfficeDev/Project-Accelerator/blob/main/releases/Project_for_the_Web_Accelerator_report.pbit?raw=true) for the Accelerator.
2. Deploy it using Power BI Desktop or in the [PowerBI.com service](https://www.powerbi.com).
3. When prompted for the environment url, use the base url of your environment. For example: `https://myenvironment.crm.dynamics.com`

When you deploy the report, ensure that your team will have access to it. [Learn more about sharing in Power BI](https://docs.microsoft.com/power-bi/collaborate-share/service-share-dashboards).

### Instructions to modify the Project Accelerator to use the deployed template

The Accelerator already contains a placeholder for the Power BI template. Once you've deployed the Accelerator and the Power BI template, follow these steps to have the Power BI report appear in the Accelerator.

1. Once you've deployed the Power BI template, open the report in [PowerBI.com](https://www.powerbi.com).
2. Press the _File_ button in the top navigation bar, open the _Embed report_ menu item, and then choose the _Website or portal_ option.

![The website or portal menu option under the share button](images/share-powerbi-report.png)

1. Copy the link in the top box ("Here's a link you can use to embed content") and keep it handy.

![Embed link](images/reports-link-code.png)

4. In a new browser tab, sign into [powerapps.com](https://make.powerapps.com).
5. In the top header, open the _Environment_ menu and select the environment you have the Project solution installed in.
6. On the left navigation, click the _Solutions_ menu item.
7. Click the _Project for the web Accelerator_ solution name to open the solution.

![Project for the web Accelerator solution](images/solution-title.png)

8. Click the _Reports_ item. It has the name _proj_Reports_ and is of type _Customization.Type_WebResource_.

![Reports item in the solution](images/reports-item.png)

9. In the new tab that opens, click the _Text Editor_ button in the _Content_ section of the page.

![Reports text editor](images/reports-text-editor.png)

10. Switch to the _Source_ tab in the dialog that appears.

![Source Tab](images/source-tab-button.png)

11. Delete the all the content in that text box and paste in the code snipped below. Replace the text between quotes `REPLACE THIS` with the link from step 3 that you created in the PowerBI.com site. Be sure to keep the quotes!

```
  <html>
    <head>
    </head>
    <body onfocusout="parent.setEmailRange();" style="overflow-wrap: break-word;">
      <iframe width="100%" height="100%" src="REPLACE THIS" frameborder="0" allowfullscreen="true"></iframe>
    </body>
  </html>
```

1.  Press _OK_ to save the changes and close the dialog.
2.  Press the _Save_ button and then the _Publish all customizations_ button to have the changes made. Once published, you can close the browser tabs.

![Save and Publish buttons](images/save-changes-for-reports.png)

**You can now view the Power BI report within the Accelerator! Just open the Reports link in the left navigation of the Project Power App**

![Power BI reports in the Project Power App](images/powerbi-in-app.png)

## Licensing

The Accelerator solution and Power BI template are distributed free of charge under the MIT license.
However, using them in your environments to work with _Project for the web_ has certain licensing implications.

Refer to the [Project Service Description](https://docs.microsoft.com/office365/servicedescriptions/project-online-service-description/project-online-service-description) for details about Project licensing.

### Using the Accelerator without the Power BI content pack

Using all the customizations -except the reports- requires a **Project Plan 1** license. This applies to your project managers who also need to do things like organize programs, track issues and risks, manage the business case and financials, or edit the custom columns such as corporate sponsor of the project.

Users who don't need to make any changes to the project and only need to view things like risks and issues need a **Microsoft 365 license**.

### Using the Accelerator with the Power BI content pack

Users who need to view the Power BI reports in the Project Accelerator need the following
1.  an M365 or Project Plan 1 license
2.  a Power BI license

### Using the Accelerator without using Project for the web

All the content on this site is completely free for you to reuse in your own applications. Refer to the [LICENSE](LICENSE) file for details. It is only when using the Accelerator with the Project Power App or when using the Project for the web tables that there are additional licensing implications.

## Support and Troubleshooting

For support of the Accelerator you can either raise an issue here in Github or open a new service request through the Microsoft 365 admin center Support tab. Microsoft fully support the deployment and use of the Accelerator with Project for the web, however we do not support any subsequent customizations that either you or a partner may have added on top of the Accelerator. We would of course still support the core functionality even if customizations have been added.

For best experience to avoid any issues with subsequent releases of the Accelerator always follow best practices of using managed solutions for any additional customization. [Learn about using solutions](https://docs.microsoft.com/powerapps/maker/data-platform/solutions-overview) and related documents for guidance on working with solutions and understanding correct use of solution layers.

### Errors about Dependencies
If you get an error (shown below) that you need a version of msdyn_ProjectServiceCore > 1.0.0.87, navigate to your list of solutions for your environment in [Power Apps](https://make.powerapps.com) and ensure that the latest version of the Project Service Core solution is installed. You'll see an "Update" option next to the solution name if there is an update available. After the update is complete, try installing the Accelerator package again.
![Power BI reports in the Project Power App](images/../dependency-error.png)