pipeline {
    agent any
       tools{
           maven "Maven"
              }
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'code_pull_github', url: 'https://github.com/syed98089/ansible_project.git']]]) 
                }
                }
             

         stage('Build for package artifact') {
            steps {
                sh 'mvn clean package'
                }
               }
}
}
