pipeline {
    agent{
        label 'wslave'
    }
    stages {

        stage('pull') {
            steps {
                git branch: 'main', url: 'https://github.com/Dilip-Singh-R/Amazon-Jenkins.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }


        
        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }

    }

  post{
    
  failure{
       echo 'Failure in the build'
   }

  }


}
