# jira-influx: Collect JIRA issue metrics and write them to InfluxDB
This tool counts issues for different JQL Queries and writes the results to InfluxDB using measurement `issue_count` and custom tags.

## Installation
Configure your `GOPATH` and run `go get github.com/cbonitz/jira-influx`

## Usage
Create a configuration file, then just run `jira-influx`

## Configuration
Create a `config.json` file with the same structure as `config.json.sample`.
Most configuration parameters are self explanatory, please see the sample file for details and the following remarks:
* JIRA: `jiraUrl` - the JIRA base URL, `jiraUsername`, `jiraPassword`
* InfluxDB: `influxUrl` - the Influx base URL, `InfluxDB` - the database to use, `influxUsername` (optional), `influxPassword` (optional)
* Queries: Each query has `jql`, a JQL query, and `tags`, the tags used for InfluxDB