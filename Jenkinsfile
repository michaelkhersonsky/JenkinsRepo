pipeline {
    agent {
        docker {
            reuseNode true
            image 'centos'
           
          
        }
    }
    stages {
        stage('Build') {
            steps {
                sh '[ -e /etc/querty.txt ] && cat /etc/release.txt || cat /etc/os-release > /etc/release.txt'
               
            }
        }
    }
}
