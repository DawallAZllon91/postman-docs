---
title: "Secret Scanner"
updated: 2023-09-15
contextual_links:
  - type: section
    name: "Additional resources"
  - type: subtitle
    name: "Videos"
  - type: link
    name: "Postman Token Scanner | Postman Level Up"
    url: "https://youtu.be/9XxkqPQF-Rw"
  - type: link
    name: "Securing APIs | Postman Enterprise"
    url: "https://youtu.be/tiYgp4QEwZQ"
  - type: subtitle
    name: "Blog posts"
  - type: link
    name: "How we’re protecting your Postman API keys in GitLab"
    url: "https://blog.postman.com/protecting-your-postman-api-keys-in-gitlab/"
  - type: link
    name: "2 Big Improvements to the Postman Token Scanner"
    url: "https://blog.postman.com/2-big-improvements-to-the-postman-token-scanner/"
  - type: subtitle
    name: "Public workspaces"
  - type: link
    name: "Postman Security"
    url:  "https://www.postman.com/postman/workspace/62d58d93-7e0c-45bf-9daa-cc8e531fc344"
---

The Postman Secret Scanner scans public workspaces to detect any exposed secrets. It checks all of the collections, global variables, environment variables, API schemas, and documentation in a public workspace to safeguard your organization from potential threats and prevent malicious users from accessing any exposed secrets.

The Secret Scanner is available on all Postman plans and is turned on by default. If you're on an [Enterprise Ultimate plan](https://www.postman.com/pricing), Secret Scanner will monitor team workspaces in addition to public workspaces.

## Contents

* [How Secret Scanner works](#how-secret-scanner-works)
* [Secret Scanner dashboard](#secret-scanner-dashboard)
    * [Resolve detected secrets](#resolve-detected-secrets)
* [Manage Secret Scanner findings with the Postman API](#manage-secret-scanner-findings-with-the-postman-api)
* [Supported secrets](#supported-secrets)
    * [Default alerts](#default-alerts)
    * [Custom alerts](#custom-alerts)
* [Protect Postman API keys in GitHub](#protect-postman-api-keys-in-github)
* [Protect Postman API keys in GitLab](#protect-postman-api-keys-in-gitlab)

## How Secret Scanner works

Postman's secret scanner follows all updates made by team members and scans them for [supported secrets](#supported-secrets).

Secret Scanner is turned on by default for all Postman teams and will monitor your team's public workspaces, collections, environments, and documentation for exposed secrets. If you're on an [Enterprise Ultimate plan](https://www.postman.com/pricing), Secret Scanner will also monitor collections and APIs in your team workspaces.

Postman delivers scan results in the [Secret Scanner dashboard](https://go.postman.co/settings/team/secret-scanner/). If an exposed secret is found, Postman notifies you by email and in-app notification. You can also set up Postman's [Slack integration](/docs/integrations/available-integrations/slack/) to alert you in Slack if this occurs.

## Secret Scanner dashboard

> **[The Secret Scanner dashboard is available on Postman Enterprise Ultimate plans.](https://www.postman.com/pricing/)**

You can view detected secrets, configure [default](#default-alerts) and [custom](#custom-alerts) alerts, and review [Secret Scanner reports](/docs/reports/security-audit-reports/) in the [Secret Scanner dashboard](https://go.postman.co/settings/team/secret-scanner/). To open the dashboard, select **Team > Team Settings** in the Postman header. Then, select **Secret Scanner** in the left sidebar.

<img alt="Secret Scanner dashboard" src="https://assets.postman.com/postman-docs/v10/secret-scanner-dashboard2-v10.18.jpg"/>

### Resolve detected secrets

Team Admins and [Super Admins](/docs/collaborating-in-postman/roles-and-permissions/#team-roles) can review the [default](#default-alerts) and [custom](#custom-alerts) secrets that the Secret Scanner has found in public and team workspaces in the **Secrets detected** tab of the [Secret Scanner dashboard](https://go.postman.co/settings/team/secret-scanner/findings). You can filter findings by workspace visibility type, workspace name, and secret type. To view the details for a detected secret, select it from the list.

> Admins and Super Admins can access all identified secrets within a team, including ones in public workspaces. Workspace Admins can also view secrets within the workspaces they manage.

<img alt="Resolve detected secret" src="https://assets.postman.com/postman-docs/v10/secret-scanner-view-detected-secret-v10.18.jpg"/>

Each detected secret shows where it was found and when it was detected. To view the SHA256 hash value of a detected secret, hover over the partially hidden value under its name and select the information icon <img alt="Information icon" src="https://assets.postman.com/postman-docs/icon-information-v9-5.jpg#icon" width="16px">.

To resolve a detected secret, select **Unresolved** and then select the reason for resolving it. You can resolve a finding with the following reasons:

* **Revoked** - This secret has been revoked.
* **False positive** - This secret is not valid.
* **Won't fix** - This secret is not relevant.

<img alt="Resolve detected secret" src="https://assets.postman.com/postman-docs/v10/secret-scanner-resolve-detected-secret-v10.18.jpg"/>

## Manage Secret Scanner findings with the Postman API

Team Admins, Super Admins, and Workspace Admins can access Secret Scanner findings through the Postman API. Using the Postman API enables you to create custom automated workflows to retrieve and resolve identified secrets. To learn more, see the [Postman API documentation](https://go.pstmn.io/live-docs-api).

## Supported secrets

The Secret Scanner scans for a variety of secrets [by default](#default-alerts). You can also add your team's proprietary third-party app tokens that aren't supported yet using [custom alerts](#custom-alerts).

### Default alerts

By default, the Secret Scanner checks for tokens issued by common service providers including Amazon, Google, GitHub, Stripe, and Twilio. To view the complete list of default alerts, open the [Secret Scanner](https://go.postman.co/settings/team/secret-scanner/alerts) and select **Configure alerts**.

### Custom alerts

> **[Custom alerts are available on Postman Enterprise plans.](https://www.postman.com/pricing/)**

You can use custom alerts to scan your team's proprietary tokens and any third-party app tokens that aren't scanned by default.

Your team can add a total of five alerts. You must be a Community Manager or team member with both Developer and Admin roles to add custom alerts.

To add custom alerts, do the following:

1. Open Postman and select **Team > Team Settings** in the Postman header. Select **Secret Scanner** in the left sidebar, then select the **Configure alerts** tab.
2. In the **Custom alerts** section, select **+ Add Alert**.
3. Add the details for the custom token, then select **Create Alert**.

## Protect Postman API keys in GitHub

Postman also works with GitHub to ensure that your Postman API keys are secure. If you commit a valid Postman API key to a public GitHub repository, Postman notifies you by email and in-app notification. You can also set up Postman's [Slack integration](/docs/integrations/available-integrations/slack/) to alert you in Slack if this occurs.

It's recommended you delete the exposed API key in your [API keys dashboard](https://go.postman.co/settings/me/api-keys). You can then [generate a new API key](/docs/developer/postman-api/authentication/#generate-a-postman-api-key) to continue working with the Postman API.

## Protect Postman API keys in GitLab

> This feature is available on GitLab Ultimate plans.

Postman works with GitLab to protect your Postman API keys in GitLab public repositories. If you accidentally commit a valid Postman API key to a public GitLab repository, Postman notifies you by email and in-app notification.

It's recommended you delete the exposed API key in your [API keys dashboard](https://go.postman.co/settings/me/api-keys) immediately. You can then [generate a new API key](/docs/developer/postman-api/authentication/#generate-a-postman-api-key) to continue working with the Postman API.
