
## FLOW

check in -> github / repo/ org/ branch, etc.
trigger/ webhook
read config (source code repo <-> event repo) -> check out an event repo
read buildflow under event repo
follow buildflow to check out source code
prepare builder
run the steps under the jobs
feedback the result to github /PR ...
notify email, slack, bugtracker, etc.

### create a jenkins job
#### with jenkins-job-builder
https://groups.google.com/g/jenkinsci-users/c/hJk2UWd-EgM

#### with REST API
https://support.cloudbees.com/hc/en-us/articles/220857567-How-to-create-a-job-using-the-REST-API-and-cURL-

#### with DSL
https://www.digitalocean.com/community/tutorials/how-to-automate-jenkins-job-configuration-using-job-dsl


### build a github action
https://deborah-digges.github.io/2020/10/14/Building-a-Github-action/


## REFERENCEs:
https://netflix.github.io/conductor/architecture/
https://netflix.github.io/conductor/configuration/eventhandlers/#event-handler