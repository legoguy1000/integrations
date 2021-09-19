# GitLab Integration

This is an integration for Gitlab. It parses JOSN formatted GitLab server logs.  
The documentation for GitLab logs is [here](https://docs.gitlab.com/ee/administration/logs.html).

## Compatibility
This module has been developed against Gitlab 14.2.4-ee, but is expected to
work with other versions of Gitlab. Some logs may not be produced in older versions, check the link above for more details

## Logs

### Production

The `production` dataset collects the `production_json.log` file. It contains a structured log for Rails controller requests received from GitLab, thanks to Lograge. Requests from the API are logged to a separate file in api_json.log.  See [here](https://docs.gitlab.com/ee/administration/logs.html#production_jsonlog) for more information.

{{fields "production"}}
