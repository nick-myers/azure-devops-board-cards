# azure-devops-board-cards
Azure DevOps Extension for printing work items to place on physical boards

https://marketplace.visualstudio.com/items?itemName=NickMyers.board-cards

## Overview

This is a very simple Azure DevOps extension which adds a "Print" tab to Sprint boards, which displays all the work items in @currentIteration and triggers the browsers print dailog.

![Print tab](/images/print-tab-in-azure-devops.png)

The extension is currently optmised for A4 portrait printing, 3 colums and 5 rows per page, and has a hard-coded set of styles (see css/cards.css) which provide formatting for different work item types.

I hope in future I'll be able to modify the extension to make configurable by end users and automatically identify the work item types.

### Example output

Following are two screenshots of the print output; I've had to obfuscate some of the content due to it being sensitive.

![Print example 1](/images/print-example-1.png)
![Print example 2](/images/print-example-2.png)

## How to build the package

Windows Powershell 
tfx extension create --manifest-globs vss-extension-dev.json --rev-version

remove the -dev extension in order to build a package for production