# Jenkins CI/CD pipelines for a real architecture but showing as example

This are pipelines for a small infrastructure scripts to be run on jenkins.

CI:
- backend: pipeline for building docker image and push to ecr.
The idea is to setup webhook on bitbucket so this runs automatically.

Deploy:
- backend: in this approach involves tagging to latest and forcing ecs service restart (if setup correctly this doesn't have downtime)
- frontend: builds vue (quasar) spa app, and copy static files to s3 with env file (no sensitive information)

