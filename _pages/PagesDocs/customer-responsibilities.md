---
title: Customer Responsibilities
permalink: /documentation/customer-responsibilities/
layout: page
sidenav: documentation
redirect_from:
  - /pages/using-federalist/customer-responsibilities/
---


## Your Responsibilities

Using Federalist places certain responsibilities on you as the government user of Federalist. GSA has many internal sites running on Federalist, but GSA cannot guarantee that Federalist is compatable with your agency's specific policies.

Federalist retains other responsibilities, clarified below. The intent of these policies is to empower you to use Federalist to its full potential with awareness of your responsibilities when using advanced features.

#### You must use a GitHub account to log onto Federalist.

Federalist is a service that leverages GitHub repositories for publishing. Federalist eliminates redundancy by allowing GitHub users with editing access to a repository to configure the site on Federalist. This requires Federalist users to authorize the Federalist application on their GitHub account **and** for Federalist to be approved by the parent organizations of repos that are hosted with Federalist. Federalist users must also have two factor authentication enabled for their GitHub accounts in order to be given access.

GitHub is used across the government (see [this dashboard](https://gsa.github.io/github-federal-stats/) from our partners in GSA's Office of Government-wide Policy), and a majority of cabinet agencies have a GitHub presence. However, GSA does not endorse Github and there are other ways to launch sites if your agency is not prepared to use GitHub. At this time, no prospective Federalist customer has been deterred by integration with GitHub.

#### You own your content

Federalist provides templates for you to start with in configuring your sites, but is not responsible for editing or updating the content or local configuration of your site. The Federalist team ensures that the publishing mechanism remains available to you so that your content edits can be published within minutes. Your content must be low impact according to [FIPS 199](http://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.199.pdf) and each branch on GitHub is published publicly by Federalist. Federalist is not suitable for hosting the following types of information:
- PII (Personally Identifiable Information)
- FOUO (For Official Use Only)
- CUI (Confidential Unclassified Information)
- Classified Information
- other content that otherwise requires authorization to view

Federalist suggests that you add your point of contact to your repo with editing rights for troubleshooting purposes, but this is not required.

#### You own your code

You may wish to use Jekyll plugins, Google Analytics from GSA's [Digital Analytics Program](https://www.digitalgov.gov/services/dap/) using embedded Javascript, or other code on your site. Federalist makes this possible - we use analytics extensively on our sites - but you are responsible for the security and stability of any custom code.

You are responsible for ensuring compliance with any and all additional federal regulations, including the [21st Century IDEA](https://digital.gov/resources/21st-century-integrated-digital-experience-act/).

#### You own your domain and DNS

Federalist does not manage your domain name nor provide DNS services. To launch a site on Federalist, you must configure the DNS for your domain to point to a domain provided by the Federalist team (meaning, that visitors to that address will be pointed at Federalist so they can load your site from us). Setting DNS for a new or existing domain may involve working with other offices at your agency; these processes typically vary.

If your domain is not an apex (e.g. 2nd level) domain, the process may be more challenging as some DNS providers do not support all required DNS record types. We recommend that you plan a solution before signing an agreement, please see [custom domains](/documentation/custom-domains) for more details.

##### SPF and DMARC records
GSA IT requires that your your URL's apex domain has appropriately set DMARC and SPF records in accordance with [BOD 18-01](https://cyber.dhs.gov/bod/18-01/).  

Expected DMARC record:
>v=DMARC1; p=reject; pct=100; fo=1; ri=86400; rua=mailto:dmarcreports@gsa.gov,mailto:reports@dmarc.cyber.dhs.gov; ruf=mailto:dmarcfailures@gsa.gov

Expected SPF record:
>v=spf1 -all

## Federalist's Responsibilities

#### We control access to the core Federalist codebase.

Access to Federalist's configuration tools for your specific content does not grant you access to Federalist's "backend." Federalist's code is open source, but only approved members of the Federalist team are allowed to make or approve changes. No one can access Federalist's management tools in [cloud.gov](https://cloud.gov) without FedRAMP-approved two factor authentication.

#### We control access to the hosting service that serves your webpages

Federalist moves content from your GitHub repositories into a secure build process and then into a file storage system that holds your site files. The credentials for the file storage system (Amazon S3 for those familiar) are secured within cloud.gov.

#### We maintain customer build logs for 180 days
In accordance with [cloud.gov's log retention policy](https://cloud.gov/docs/deployment/logs/#web-based-logs-with-historic-log-data), we will store logs from customer builds for 180 days, after which they will no longer be available.