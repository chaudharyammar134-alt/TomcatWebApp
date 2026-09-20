pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/chaudharyammar134-alt/TomcatWebApp.git'
            }
        }

        stage('Build') {
            steps {
                bat '"C:\\Users\\HLBS\\Downloads\\apache-maven-3.9.16-bin\\apache-maven-3.9.16\\bin\\mvn.cmd" clean package'
            }
        }

        stage('Deploy') {
            steps {
                bat 'copy /Y target\\TomcatWebApp.war "C:\\Users\\HLBS\\Downloads\\apache-tomcat-10.1.60-windows-x64\\apache-tomcat-10.1.60\\webapps\\TomcatWebApp.war"'
            }
        }
    }
}