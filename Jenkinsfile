pipeline {
    agent any


    stages {
        stage ('Show commit author') {
            steps {
                sh "echo 'Hello from Hssan!'"
            }
        }
        stage ('Execute CI pipeline') {
            agent {
                docker { image 'node:8.11.2-alpine' }
            }
           
                stage('NPM build'){
                    steps {
                        sh 'npm run-script build --prod'
                    }
                }
                stage ('Artifacts') {
                    steps {
                        sh "tar czvf dist.tar.gz dist"
                        sh 'tar -czvf app.${BUILD_ID}.tar.gz dist'
                        archiveArtifacts "**/*.tar.gz"
                    }
                }
            }
        }
    }
}
