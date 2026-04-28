pipeline{
    agent any
    options {
        timeout(time: 5, unit: "MINUTES")
        timestamps()
    }
    stages {
        stage("make a directory"){
            steps{
                sh "mkdir jenkins-test"
            }
        }
        stage("add a file"){
            steps{
                sh "touch jenkins-test/file1.txt"
            }
        }
    }
    post {
        always{
            archiveArtifacts artifacts: "jenkins-test/*.txt", allowEmptyArchive: true
        }
    }


}
