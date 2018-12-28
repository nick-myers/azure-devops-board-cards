# Overview

This is a very simple Azure DevOps extension which adds a "Print" tab to Sprint boards, which displays all the work items in @currentIteration and triggers the browsers print dailog.

![Print tab](/images/print-tab-in-azure-devops.png)

The extension is currently optmised for A4 portrait printing, 3 colums and 5 rows per page, and has a hard-coded set of styles (see css/cards.css) which provide formatting for different work item types.

I hope in future I'll be able to modify the extension to make configurable by end users and automatically identify the work item types.