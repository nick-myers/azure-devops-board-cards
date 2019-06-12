# azure-devops-board-cards
Azure DevOps Extension for printing work items to place on physical boards

https://marketplace.visualstudio.com/items?itemName=NickMyers.board-cards

## Why I created this

I'm not a professional web developer, I'm a delivery manager who works with software teams and I identified a need to automate (as much as possible) the creation of physical tickets to place on physical boards (information radiators) based on the content of Azure DevOps boards.

This is very much a side project; I think it's useful enough to make available for others to use.  

## Minor version update - version 3.8 released 12th June 2019

* Includes 'Assignee' and 'Original Estimate' fields on cards
* Bug fix: removed use of clamp.js for line truncation (which was throwing an error).

## Major version update - version 3.0 released on 30th April 2019

This version includes the ability to select "small" or "large" cards for printing.

* Small - 3 x 5 cards (15 per A4 sheet)
* Large - 2 x 3 cards (6 per A4 sheet)

## Major version update - version 2.0 released on 9th April 2019

This version has been overhauled to try address some of the issues users were running into and provide some of the features requested. 

In addition to the underlying design of the code that makes the extension work being completely rebuilt, the extension now allows users to select iterations, work item types and areas to be used to filter what work items are output for printing.

Finally, the printed work items now include the parent work item ID and title, for ease of reference.

## Overview

This is a very simple Azure DevOps extension which adds a "Print" tab to Sprint boards, which displays all the work items in @currentIteration and triggers the browsers print dailog.

![Print tab](/images/print-tab-in-azure-devops.png)

### Printing

The extension is currently optmised for A4 portrait printing, 3 colums and 5 rows per page, and has a hard-coded set of styles (see css/cards.css) which provide formatting for different work item types.  

If you wish to add more styles based on your own work item types, please open and submit a pull request.

### Configuration options

![Configuration options](/images/configuration-options.png)

### Example output

Following are two screenshots of the print output; I've had to obfuscate some of the content due to it being sensitive.

![Print example 1](/images/print-example-1.png)
![Print example 2](/images/print-example-2.png)

Note - these screenshots do not show the parent work item details (ID and title) that are included.

## How to build the package

Windows Powershell 
```tfx extension create --manifest-globs vss-extension-dev.json --rev-version```

remove the -dev extension in order to build a package for production

## Github repo

https://github.com/nick-myers/azure-devops-board-cards
