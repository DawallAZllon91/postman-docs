---
title: "The Flows Interface"
updated: 2023-08-15
---

Postman flows has an easy-to-use interface to create your applications. This guide is a high-level overview of the Postman Flows interface.

<img src="https://assets.postman.com/postman-labs-docs/getting-started/flows-ui.png" alt="Flows user interface" fetchpriority="low" loading="lazy" />

## The Postman Flows user interface

* [Blocks on the canvas](#blocks-on-the-canvas)
* [Building applications](#building-applications)
* [Navigation](#navigation)

### Blocks on the canvas

The following blocks can be used to construct your application:

* **(1) The Start block:** The first block found in every flow and the only one that can't be deleted. Applications (Forms and Webhooks) send their information through this block.
* **(2) Other blocks:** One of the many types of other blocks that can be used in a flow. The list of blocks is [here](/docs/postman-flows/reference/blocks-list/).
* **(3) Text annotations:** One of the ways to document a flow for other users or explain complex tasks being performed.
* **(4) Groups:** Enables organization, documentation, and building of flows since groups can be duplicated. More information on organizing a flow can be found [here](/docs/postman-flows/concepts/organizing-a-flow/)

### Building applications

The following controls are used to build your application:

* **(5) Forms:** Create a form that runs a flow on user submission. Learn more about forms [here](/docs/postman-flows/concepts/creating-a-form/).
* **(6) Webhook-based applications:** Create a flow that either runs automatically on a schedule, or whenever a specified event happens. More information on webhooks and automatic runs can be found [here](/docs/postman-flows/concepts/automatic-runs/).
* **(7) Console:** This is where you can find all API activity. This is useful for debugging flows and ensuring your flow is running with the expected information. A guide on debugging flows can be found [here](/docs/postman-flows/reference/debugging/).

### Navigation

Navigate the canvas with the following controls:

* **(8) Toolbar**: Contains the Redo/Undo, Zoom, and Fit view buttons.
* **(9) Run:** Runs the flow.
* **(10) Add annotation:** Adds a text annotation.
* **(11) Minimap:** Enables easier navigation of larger flows.