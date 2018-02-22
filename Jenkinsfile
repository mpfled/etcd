pipeline {
    agent none
    stages {
        stage('test') {
            agent {
                dockerfile { 
              filename 'Dockerfile-test' 
              dir '/go/'
              label 'etcd-test'
            }
            }
            steps {
                sh ./test
            }
        }
        stage('producto') {
            agent {
                dockerfile { 
                  filename 'Dockerfile' 
                }
            }
            steps {
                sh sleep 10
            }
        }
    }
}
