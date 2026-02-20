@Library("shared") _
pipeline {
    agent any

    stages {
        stage('ello'){
            steps{
                script{
                    hello()
                }
            }
        }
        stage('Checkout') {
            steps {
                script{
               clone ("https://github.com/JoinDevops0425/django-notes-app.git", "main")
            }
            }
        }
        stage('build') {
            steps {
               script{
                   docker_build("joindevops0425", "notesapp")
               } 
            }
        }
        stage('Push') {
            steps {
                script{
                    docker_push("notesapp")
                  }
                }
              }   
     }
}
