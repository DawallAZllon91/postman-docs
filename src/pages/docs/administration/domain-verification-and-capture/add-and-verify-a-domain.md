---
title: "Verify your organization’s domain in Postman"
updated: 2023-10-03
contextual_links:
  - type: section
    name: "Additional resources"
  - type: subtitle
    name: "Blog posts"
  - type: link
    name: "Introducing Domain Capture: Group Your Organization’s Postman Users into a Single Team"
    url: "https://blog.postman.com/introducing-domain-capture/"
---

> **[Domain verification is available on Postman Enterprise plans. Domain capture is available on Postman Enterprise Ultimate plans.](https://www.postman.com/pricing)**

To set up domain capture, you'll first need to add and verify your organization's domain or subdomain. You must be a [Team Admin](/docs/collaborating-in-postman/roles-and-permissions/#team-roles) to add and verify a domain in Postman.

## Contents

* [Why should my organization verify a domain with Postman?](#why-should-my-organization-verify-a-domain-with-postman)

* [Add and verify a domain](#add-and-verify-a-domain)

    * [Verify a domain later](#verify-a-domain-later)

    * [View verification details](#view-verification-details)

    * [View unclaimed accounts](#view-unclaimed-accounts)

* [Enable domain capture](#enable-domain-capture)

## Why should my organization verify a domain with Postman?

Adding and verifying a domain enables Postman to implicitly trust your team and its connection to your organization. It's required to turn on [domain capture](/docs/administration/domain-verification-and-capture/domain-capture-overview/#why-should-my-organization-enable-domain-capture-in-postman), but it also improves the onboarding process as you continue to grow your Postman team.

Without a verified domain, individual accounts that you invite to your team are given the option to join or dismiss the invite. If they choose to join, they're also required to reauthenticate prior to accessing the team. By verifying your organization's domain, it removes the friction of adding users who have already verified their email addresses with the relevant domain when they created Postman accounts. Postman will no longer require users' permission to join your team, letting you instantly provide new teammates with all of the resources they’ll need to be successful contributors.

> For more information on the benefits of enabling domain capture, see [Why should my organization enable domain capture in Postman?](/docs/administration/domain-verification-and-capture/domain-capture-overview/#why-should-my-organization-enable-domain-capture-in-postman)

## Add and verify a domain

As a [Team Admin](/docs/collaborating-in-postman/roles-and-permissions/#team-roles), you can add domains and subdomains to your team in your [Admin dashboard](https://go.postman.co/settings/team/domain-capture).

1. Open Postman and select **Team > Team Settings** in the Postman header. Select **Authentication** in the left sidebar.

1. Select the **Domains** tab.

1. Select **Add Domain**.

    ![Select Add Domain](https://assets.postman.com/postman-docs/v10/authentication-add-domain-v10.18.jpg)

1. Enter the domain or subdomain you'd like to add. If you're adding a subdomain, you can choose to verify it through the root domain's verification record or through a verification record that's unique to the subdomain. Select **Continue**.

    <img alt="Add domain" src="https://assets.postman.com/postman-docs/v10/add-domain-verify-root-v10.18.jpg" width="450px"/>

    > If you're adding a subdomain and its root domain has already been verified by Postman, you'll see a **VERIFIED** status next to the root domain. If you choose to verify through the root domain, you won't need to add any additional TXT records to your DNS configuration after you select **Continue**.

1. Select <img alt="Copy icon" src="https://assets.postman.com/postman-docs/icon-copy-v9.jpg#icon" width="15px"> **Copy** to copy the **TXT Record**, then add it to your domain's DNS configuration. If you've chosen to verify a subdomain directly without the use of the root domain, you must enter the subdomain in your DNS host before you add the TXT Record.

    > If you're not ready to add the **TXT Record** to your domain's DNS configuration, you can select **Verify Later**. For next steps, see [Verify a domain later](#verify-a-domain-later).

1. Select the **I have added the TXT record to the DNS tool** checkbox, and then select **Verify Domain**.

    <img alt="Add TXT record and verify domain" src="https://assets.postman.com/postman-docs/v10/verify-domain-v10.18.jpg" width="450px"/>

    > It may take up to 24 hours for the TXT changes to take effect to enable successful verification of the domain. Team Admins will receive an email notification when the domain is verified.

1. Once your domain is verified, you can [view unclaimed accounts](#view-unclaimed-accounts) and [request to enable domain capture](#enable-domain-capture).

> If you're unable to verify your domain in Postman, please contact your Customer Success Manager or [Postman support](https://www.postman.com/support/) for assistance.

### Verify a domain later

Optionally, you can verify a domain later if you didn't verify the domain when you added it.

To verify a domain you've already added, do the following:

1. Open Postman and select **Team > Team Settings** in the Postman header. Select **Authentication** in the left sidebar, then select the **Domains** tab.

1. Select **Verify** next to the domain with the **UNVERIFIED** status you want to verify.

    > You can also select **Manage** next to the domain with the **UNVERIFIED** status you want to verify, then select **View Verification Details**.

    ![Verify domain later](https://assets.postman.com/postman-docs/v10/verify-domain-later-v10.18.0.jpg)

1. Select <img alt="Copy icon" src="https://assets.postman.com/postman-docs/icon-copy-v9.jpg#icon" width="15px"> **Copy** to copy the **TXT Record**, and then add it to your domain's DNS configuration. If you've chosen to verify a subdomain directly without the use of the root domain, you must enter the subdomain in your DNS host before you add the TXT Record.

1. Select the **I have added the TXT record to the DNS tool** checkbox, and then select **Verify Domain**.

    <img alt="Verify unverified domain" src="https://assets.postman.com/postman-docs/v10/verify-unverified-domain-later-v10.18.jpg" width="450px"/>

    > It may take up to 24 hours for the TXT changes to take effect to enable successful verification of the domain. Team Admins will receive an email notification when the domain is verified.

1. Once your domain is verified, you can [view unclaimed accounts](#view-unclaimed-accounts) and [request to enable domain capture](#enable-domain-capture).

### View verification details

Team Admins can view verification details for verified and unverified domains in the [domain dashboard](https://go.postman.co/settings/team/domain-capture). Verification details include the verification **TXT Record**.

1. Open Postman and select **Team > Team Settings** in the Postman header. Select **Authentication** in the left sidebar, then select the **Domains** tab.
1. Select **Manage** next to the domain you want to view verification details for.
1. Select **View Verification Details**.

### View unclaimed accounts

Unclaimed accounts are accounts associated with a verified domain that haven't signed in since domain capture was enabled and aren't yet part of your team. Team Admins can view unclaimed accounts in the [domain dashboard](https://go.postman.co/settings/team/domain-capture).

1. Open Postman and select **Team > Team Settings** in the Postman header. Select **Authentication** in the left sidebar, then select the **Domains** tab.
1. Select **Manage** next to the domain with the **VERIFIED** status you want to view unclaimed accounts for, and then select **View Accounts**.

    > Optionally, you can select the number of unclaimed accounts next to the domain in the domain dashboard.

1. View the list of accounts not part of your team.

    <img alt="View unclaimed accounts" src="https://assets.postman.com/postman-docs/v10/view-unclaimed-accounts-v10.jpg" width="450px"/>

1. Optionally, you can select **Export CSV** to export the list as a CSV file. You will receive an email containing the download link.

## Enable domain capture

Now that you've added and verified a domain, you can [enable domain capture](/docs/administration/domain-verification-and-capture/enable-domain-capture/).
