#!groovy
pipeline {
    environment {
  registry = 'Nithishkumar0064/jenkinsfile.groovy'
  registryCredentials = 'none'
 }
    agent any
    stages{
        stage('Clone the Git Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Nithishkumar0064/new-java-project.git'
            }
        }
        stage('Build'){
            steps {
                script {
                    sh mvn clean install
                }
            }
        }
        stage('Push image to Hub'){
            steps {
                sh 'echo Registry-push'
				
                }
            }
        }
        stage('Deploy to tomcat') {
            steps {
                sh 'sudo cp /home/ubuntu/new-folder/workspace/assignment-scripted/target/*.jar  /opt/tomcat/apache-tomcat-9.0.68/webapps/'
            }
            
        }
        
    }
