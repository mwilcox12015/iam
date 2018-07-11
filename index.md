---

copyright:

  years: 2017, 2018

lastupdated: "2018-04-05"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} Identity and Access Management
{: #iamoverview}

## What is Cloud IAM?

{{site.data.keyword.Bluemix_notm}}  Identity and Access Management (IAM) is an authorization service used for user and service role based access control (RBAC) in IBM Cloud. For example the IBM Cloud Appid service performs user authentication while IAM provides RBAC after the user or service has been 'authenticated.  A set of {{site.data.keyword.Bluemix_notm}} services are enabled to use Cloud IAM for access control and are organized into [resource groups](/docs/account/resourcegroups.html) within your account to enable giving users quick and easy access to more than one resource at a time. Cloud IAM access policies are used to assign users and service IDs access to the resources within your account. You can group a set of users and service IDs into an [access group](/docs/iam/groups.html) to easily give all entities within the group the same level access.

A policy assigns a user or [service ID](/docs/iam/serviceid.html#serviceids) one or more roles with a combination of attributes that define the scope of access. The policy can provide access to a single service down to the instance level, or the policy can apply to a set of resources organized together in a resource group. Depending on the [user roles](/docs/iam/users_roles.html#iamusermanrol) that you assign, the user or service ID is allowed varying levels of access for completing platform management tasks or accessing a service by using the UI or performing specific types of API calls.

![IAM for access control in an account](images/iam-diagram.svg "How access management works in an account by using IAM")

For services that do not support creating Cloud IAM policies for managing access, you can use [Cloud Foundry access](/docs/iam/cfaccess.html#cfaccess).


## What features does Cloud IAM provide?
{: #features}

<dl>
<dt>User management</dt>
<dd>Unified user management enables you to add and delete users in an account for both platform and infrastructure services. You can create a group of users called an access group to make assigning access for more than one user at a time a quick and easy task.</dd>
<dt>Fine-grained access control</dt>
<dd>Access for users and service IDs is defined by a policy. Within the policy, the scope of access for a user, service ID, or access group can be assigned to a set of resources in a resource group or a single resource. After the scope is set, you can define what actions are allowed by the subject of the policy by selecting access roles. Roles provide a way to tailor the level of access that is granted for the subject of the policy to perform platform management tasks and access a service's UI or perform API calls.</dd>
<dt>API keys for user authentication</dt>
<dd>Multiple API keys can be created for a user to support key rotation scenarios, and the same key can be used for accessing  multiple services. Platform user API keys enable users who use two-factor authentication or a federated ID to automate authentication from the command line.</dd>
<dt>Service IDs</dt>
<dd>A service ID identifies a service or application similar to how a user ID identifies a user. These are IDs that can be used by applications to authenticate with an {{site.data.keyword.Bluemix_notm}} service. Policies can be assigned to each service ID to control the level of access that is allowed by an application using the service ID, and an API key can be created to enable the authentication.</dd>
</dl>


## How do I use Cloud IAM?

You can access and use Cloud IAM through the Identity and Access UI or the CLI for {{site.data.keyword.Bluemix_notm}}.

To access Cloud IAM by using the UI, go to **Manage** &gt; **Security** &gt; **Identity and Access**.

To access Cloud IAM by using the CLI, refer to [Commands for managing API keys and policies](/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_iam).
