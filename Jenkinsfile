pipeline {
    agent {
        label 'docker-maven-slave1'
    }
    
    tools {
        maven 'maven1'
    }

    stages {
    stage('Source Control Mgnt') {
            steps {
                git branch: 'main', credentialsId: '54d6a6bc-c70b-44a7-9db6-fcb5d9f66131', url: 'https://github.optum.com/kbisen1/MyTestRepo.git'
            }
        } 
  /*  stage('Source Control Mgnt') {
            steps {
                git credentialsId: '54d6a6bc-c70b-44a7-9db6-fcb5d9f66131', url: 'https://github.optum.com/kbisen1/MyTestRepo.git'
            }
        }    */
    
    stage('Build the JAR') {
            steps {
                sh label: '', script: 'mvn clean package install'
            }
        }
        
 /*   stage('Build the JAR') {
            steps {
                script {
                sh '''mvn clean package install'''
              }
            }
        }    */
        
/*    stage('Build Docker Image') {
            steps {
                sh label: '', script: '''echo Kshitij
                                ls -ltr
                            docker build -t  myimage:dev .
                            '''
            }    
        } */
    
/*    stage('Start Docker Container') {
            steps {
                sh label: '', script: '''
                            docker run --name maventest_container myimage:dev
                            '''
            }    
        } */
    
 /*   stage('Deploy JAR') {
            steps {
                sh label: '', script: '''
                            cd "${WORKSPACE}/target"
                            java -cp test-maven-0.0.1.jar com.optum.rxclaim.App
                            '''
            }    
        }    */
        
    }
}
