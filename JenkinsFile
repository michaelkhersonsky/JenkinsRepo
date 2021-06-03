pipeline {
        agent any
        stages {
            stage('Build') {
            steps {
                echo 'Hi, this is our build step...'
            }
        }

            stage('Test') {
            steps {
                echo 'this is our testing step'

            }
        }

            stage('Deploy') {
                parallel {
                    stage('Start Deploy') {
                        steps {
                            echo " We are starting docker deployment"
                }
                }
                    stage('Deploying now') {
                    agent {
                        docker {
                            reuseNode true
                            image 'nginx'
                    }
                }
                        steps {
                            echo "We have completed Deployment"
                }
                }
            }
        }    
    }
}
