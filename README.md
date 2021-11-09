# connectall-gitlab-adapter
GITLAB Adapter for ConnectALL

## Description
ConnectALL's GitLab adapter is a configuration of ConnectALL's Universal Adapter

## Supported Entity Type
* GitLab Issues

## Examples
* Issues reported by the community will be synchronized to Jira (or another application of your choosing) for planning and tracking

# How to use

> Please reach out to sales@connectall.com for a trial license.

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
