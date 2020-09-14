# gitwebhook jenkins
# Build Periodically
# Poll SCM
# Build After other projects
# Trigger build remotely
# GitHub Hook SCM Polling (Working)
## ngrok
## smee.io
## added domain name
### Working for boths
### Checking our domain
# Email Notification
## testing
### Not Working...
# PipleLines
## Simple working...
### Triggering Pipeline Builds (Scriptive language)
## Repo Changed to public (Worked)
## Created another job with ssh url and cred
# Edited script and Now its working with private as well
# triggering code for private repo with ssh creds and ssh url using scripted pipeline
properties([pipelineTriggers([githubPush()])])

node {
    git url: 'git@github.com:ahmedbutt7121991/gitwebhook.git', credentialsId: 'gitcred'
    
    stage('Hello') {
        if (env.BRANCH_NAME == 'master')
        {
            echo 'Hello ${BRANCH}'
        }
        else {
            echo 'Warning.....'
        }
    }
    stage('Triggering') {
        echo 'Triggering Using GITHOOK....'
    }
}
# Master Slave Architecture in Docker using On demand method
## Agent1 and Agent2 are added
### Run 2 spearate jobs on 2 separate Agents on Same Trigger
