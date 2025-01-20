pipeline {  

    agent any
        
    tools{
        maven "Maven2"
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

        stage('Deploy to Tomcat Server'){
        steps{
        deploy adapters: [tomcat9(credentialsId: 'e1d11576-b08e-4418-9415-9571e7bba8eb', path: '', url: 'http://10.0.0.86:8080/')], contextPath: 'maven-web-app', war: '**/*.war'
        
    }
}
