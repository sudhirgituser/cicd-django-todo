pipeline {
    agent any

    stages {
        stage('Copy The Code') {
            steps {
               git url: "https://github.com/atharva5683/django-todo.git" , branch: "devops"
            }
        }
        stage('Build The Code') {
            steps {
               sh "docker build . -t django-todo"
            }
        }
        stage('Test The Code') {
            steps {
               echo"Test the code"
            }
        }
        stage('Deploy The Code') {
            steps {
               sh "docker run -d -p 8000:8000 django-todo "
            }
        }
    }
    
}
