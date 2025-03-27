# ua-GitLab

The ConnectALL GitLab Universal Adapter is developed as an extension to the universal adapter capability of ConnectALL. This adapter will allow the user to use GitLab with ConnectALL. Current capabilities and limitations will be defined below.

Please refer to the [ConnectALL Tech Docs](https://techdocs.broadcom.com/us/en/ca-enterprise-software/valueops/connectall/3-5/adapters/universal-adapter.html) for more information.

If you are an existing SaaS customer, please contact Broadcom Support to enable the adapter in your environment. If you are using ConnectALL On-Premise, you may download and install this adapter in your environment. If you are not yet a customer, [please reach out to learn more](https://enterprise-software.broadcom.com/contact-us).

# Setup

## Supported Entities

This Universal Adapter currently supports the following entities:
* Issues
* Branches
* Commmits
* Merge Requests
* Deploys

*Note: This Universal Adapter is provided as-is. It is tested and validated using the entities and configurations as defined. Any additional customizations are not supported and should be made at your own discretion.*

## Connection Details

* **Connection Name:** *GiLab*
* **Application Type:** *gitlab*
* **URL:** *Base URL for application (ex: https://gitlab.com)*
* **User Name:** *Leave Blank. Basic Auth is not supported*
* **Password:** *Leave Blank.  Basic Auth is not supported*
* **Auth Operation:** *Header*
* **Application Category:** *Pick from dropdown list*
* **Time Zone:** *Select GMT+0 as the time zone*
* **Select Group:** *Set if neccessary*
* **Authentication Type:** *API Key*
* **API Key:** *Authorization*
* **API Value:** *Bearer <ACCESS_TOKEN>*

**Notes:**  

A group or personal access token is needed to create a valid connection.  Be sure to enter "Bearer access_token".  The space between Bearer and the token is required.  

Using a high level group access token will enable fewer ConnectALL connections to be created.  But be sure to take security best practices into account when deciding where to create the group access token.

The scope of the access token will determine which projects are listed when configuring the project entity under the **Entity Mapping** tab of the automation.  The UA adapter is currently set to query projects where **owner=true** to reduce all public projects from appearing in the dropdown list. 

## Flow Filters

Flow filters can be created by adding attributes for the specific entity as descripted in the GitLab API

As an example, to create a flow filter for a specific environment such as production for a deployment entity:
**environment=production**

**Notes:**  

For filter names that include a space, replace the space with **%20**

For Commit entity, a flow filter could be **author=Jane%20Doe** where **%20** is used in place of a space.  

See the [GitLab API documentation](https://docs.gitlab.com/ee/api/rest/) for a list of possible flow filter entities.

## Example Automation

- Create a GitLab Issue from a ServiceNow Incident.
- Create a new Branch in GitLab when a Rally User Story or Defect reaches the "In Progress" Flow State.
- Link a Commit or a Merge Request from GitLab to a Rally User Story or Defect.
- Pull Deploy and Commit objects to support Dora4 Metrics in [Broadcom ValueOps Insights.](https://techdocs.broadcom.com/us/en/ca-enterprise-software/valueops/valueops-solution/ValueOps-Solution/n-valueops-capabilities/valueops-insights.html)

# Known Limitations

*No Known Limitations*

# Supporting Documentation

Third Party API Documentation: [Link to GitLab API Documentation](https://docs.gitlab.com/ee/api/rest/)
