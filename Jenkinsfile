pipeline {
    agent any
    
   
    
 stages {
        stage('SCM Checkout'){
      git 'https://github.com/sathishkumarkp/jenkins-pipeline-Demo'
             }
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'MAVEN3') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MAVEN3') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'MAVEN3') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
