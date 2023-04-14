pipeline {
    agent any

    stages {
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
   
  	stage('Maven Install') {
    	agent {
      	docker {
        	image 'maven:3.5.0'
        }
      }
      steps {
      	sh 'mvn clean install'
      }
    }
  }
}
