# Overview

This is a very simple Azure DevOps extension which adds a "Print" tab to Sprint boards, which displays all the work items in @currentIteration and triggers the browsers print dailog.

![Print tab](/images/print-tab-in-azure-devops.png)

The extension is currently optmised for A4 portrait printing, 3 colums and 5 rows per page, and has a hard-coded set of styles (see css/cards.css) which provide formatting for different work item types.

I hope in future I'll be able to modify the extension to make configurable by end users and automatically identify the work item types.  In the mean time if you'd like to submit PRs to include new styles (until I get the per install configuration working completely) the link to the github repo is below

## Github repo

https://github.com/nick-myers/azure-devops-board-cards

## Example output

Following are two screenshots of the print output; I've had to obfuscate some of the content due to it being sensitive.

![Print example 1](/images/print-example-1.png)
![Print example 2](/images/print-example-2.png)