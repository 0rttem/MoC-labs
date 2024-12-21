pipeline {
agent any
triggers {
cron(get_cron_string())
githubPush()
pollSCM("")
}
options {
skipDefaultCheckout(true)
parallelsAlwaysFailFast()
disableConcurrentBuilds()
buildDiscarder(logRotator(numToKeepStr: '20', artifactNumToKeepStr: '20'))
}
