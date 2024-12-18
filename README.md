# ua-GitLab

The ConnectALL GitLab Universal Adapter is developed as an extension to the universal adapter capability of ConnectALL. This adapter will allow the user to use GitLab with ConnectALL. Current capabilities and limitations will be defined below.

Please refer to the [ConnectALL Tech Docs](https://techdocs.broadcom.com/us/en/ca-enterprise-software/valueops/connectall/3-5/adapters/universal-adapter.html) for more information.

If you are an existing SaaS customer, please contact Broadcom Support to enable the adapter in your environment. If you are using ConnectALL On-Premise, you may download and install this adapter in your environment. If you are not yet a customer, [please reach out to learn more](https://enterprise-software.broadcom.com/contact-us).

# Setup

## Supported Entities

This Universal Adapter currently supports the following entities:
* GitLab Issues
* GitLab Merge Requests
* GitLab Deploys
* GitLab Commits

*Note: This Universal Adapter is provided as-is. It is tested and validated using the entities and configurations as defined. Any additional customizations are not supported and should be made at your own discretion.*

## Connection Details

* **Connection Name:** *GiLab*
* **Application Type:** *gitlab*
* **URL:** *Base URL for application (ex: https://gitlab.com)*
* **User Name:** *Set if neccessary*
* **Password:** *Set if neccessary*
* **Auth Operation:** *Header*
* **Application Category:** *Pick from dropdown list*
* **Time Zone:** *Select GMT+0 as the time zone*
* **Select Group:** *Set if neccessary*
* **Authentication Type:** *API Key*
* **API Key:** *Authorization*
* **API Value:** *Bearer: Bearer <ACCESS_TOKEN>*

**Note:**  *A group or personal access token is needed to create a valid connection.  Be sure to enter "Bearer access_token".  The space between Bearer and the token is required.  Using a high level group access token will enable fewer ConnectALL connections to be created.  But be sure to security into account when deciding where to create the group access token.*

## Flow Filters

*Flow filters can be created by adding attributes for the specific entity as descripted in the GitLab API*

*As an example, to create a flow filter for a specific environment such as production for a deployment entity:*
*environment=production*

*Note:  For filter names that include a space, replace the space with %20*

*For Commit entity, a flow filter could be author=Jane%20Doe where %20 is used in place of a space*

## Example Automation

*Provide an example of an automation*

# Known Limitations

*Enter text here describing limitations*

# Supporting Documentation

Third Party API Documentation: [Link to API Documentation](https://docs.gitlab.com/ee/api/rest/)
