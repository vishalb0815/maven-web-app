pipeline {  

    agent any
        
    tools{
        maven "Maven-3.8.7"
    }
    stages {
        stage('Clone') {
            steps {
               git 'https://github.com/ashokitschool/maven-web-app.git'
            }
        }
        stage('Build') {
            steps {
               sh 'mvn clean package'
            }
        }
    }
}
