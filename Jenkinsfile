pipeline {
    agent any
     
    stages {
        stage('Clone the project'){
            
            steps {
                https://github.com/krishnagopika/AllergyService.git'
                    }
        }
        stage('Maven Install') {
      steps {
      	sh 'mvn clean install'
      }
        stage('Docker Build') {
    	agent any
           steps {
      	    sh 'docker build -t pms:latest '
            }
         }
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying.'
            }
        }
   
  	
    }
  }
}
