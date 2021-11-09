# connectall-gitlab-adapter
GITLAB Adapter for ConnectALL


ConnectALL GitLab adapter is built on top of Universal adapter configuration.

## Usecase
GitLab issues can now be synchronized to other systems.

## Examples
* Issues reported by community will be synchronized to Jira for planning and tracking

# How to use

> In order to use the Gitlab adapter you will need to get the license from ConnectALL sales team. Please reach out to sales@connectall.com for licenses and quotes.

## Authentication
* In Gitlab, create a Personal Access Token
* In ConnectALL, navigate to `Configuration -> Connections` screen and create a new connection to Gitlab like `https://gitlab.com` as the URL
* Select GMT+0 as the time zone
* Auth Option: `Header`
* Auth Operation: `ApiKey`
* Api Key: `Authorization`
* Api Value: `Bearer <PERSONAL_TOKEN>`

## Define application links
* Create an application link in ConnectALL between Gitlab and a destination application of your choice
