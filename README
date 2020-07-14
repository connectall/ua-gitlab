# connectall-gitlab-adapter
GITLAB Adapter for ConnectALL


ConnectALL GitLab adapter is built on top of Universal adapter configuration.

## Usecase
GitLab issues can now be synchronized to other systems.

## Examples
* Issues reported by community will be synchronized to Jira for planning and tracking

# How to use

> In order to use the Gitlab adapter you will need to get the license from ConnectALL sales team. Please reach out to sales@connectall.com for licenses and quotes.

## Import specifications
* Import *-adapter-descriptor.json in to ConnectALL using "Install custom adapter" feature. Customize the descriptor after importing to fit your personal projects
* View the transformation specs and open the transformation spec page
* Choose the operation, adapter type and create draft specifications
* Import the transformation specs of {adaptertype}-{operation}-[request|response]-[groovy|jolt].[groovy|json] into ConnectALL
* Test the specifications and save them as Active

## Define application links
* Create an application link in ConnectALL between Gitlab and a destination application of your choice
* Navigate to `Configuration -> Connections` screen and create a new connection to Gitlab like `https://gitlab.com` as the endpoint
* In the Entity mapping tab under Advanced Properties choose "Sync Type" as POLL
* Use the below REST API templates for each operation

|Operation|API Method|Template|
|--- | --- | ---|
|QUERY MODIFIED RECORDS|GET|/api/v4/issues?updated_after=${last-modified-time}|
|READ RECORD BY ID|GET|/api/v4/projects/${project}/issues/${recordId}|
|CREATE RECORD|POST|/api/v4/projects/${project}/issues?${fields[ValueSeparator:'='] [FieldSeparator:'&']}|
|UPDATE RECORD|PUT|/api/v4/projects/${project}/issues/${recordId}?${fields[ValueSeparator:'='] [FieldSeparator:'&']}|
