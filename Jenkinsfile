println "URL: ${url}"
def location = (url =~ /https:\/\/[^\/]+\/[^\/]+\/([^.]+)(.git)?/)[0][1]
println "Dir: ${location}"
pipeline {
    agent any
    stages {
        stage ('Git clone') {
            steps {
                dir (location) {
                    git url:"${url}", branch: "main"
                }
            }
        }
    }
}
