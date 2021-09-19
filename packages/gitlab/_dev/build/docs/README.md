# GitLab Integration

This is an integration for Self-Hosted Gitlab. It parses JOSN formatted GitLab server logs.  
The documentation for GitLab logs is [here](https://docs.gitlab.com/ee/administration/logs.html).

## Compatibility
This module has been developed against Gitlab 14.2.4-ee, but is expected to
work with other versions of Gitlab. Some logs may not be produced in older versions, check the link above for more details

## Logs

### Production

The `production` dataset collects the `production_json.log` file. It contains a structured log for Rails controller requests received from GitLab, thanks to Lograge. Requests from the API are logged to a separate file in api_json.log.  See [here](https://docs.gitlab.com/ee/administration/logs.html#production_jsonlog) for more information.

{{fields "production"}}

### Application

The `application` dataset collects the `application_json.log` file. It helps you discover events happening in your instance such as user creation and project removal.  See [here](https://docs.gitlab.com/ee/administration/logs.html#application_jsonlog) for more information.

{{fields "application"}}

### API

The `api` dataset collects the `api_json.log` file. It helps you see requests made directly to the API. See [here](https://docs.gitlab.com/ee/administration/logs.html#api_jsonlog) for more information.

{{fields "api"}}

### Integrations

The `integrations` dataset collects the `integrations_json.log` file. It contains information about integration activities, such as Jira, Asana, and irker services. See [here](https://docs.gitlab.com/ee/administration/logs.html#integrations_jsonlog) for more information.

{{fields "integrations"}}



