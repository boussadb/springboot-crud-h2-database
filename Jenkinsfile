pipeline{
    agent any
    stages{
        stage(' Compile stage'){
        steps{
                WithMaven('maven: maven3_5_3'){
                sh 'mvn clean compile'
                 }
             }
        }

        stage(' Testing stage'){
                steps{
                        WithMaven('maven: maven3_5_3'){
                        sh 'mvn test'
                         }
                     }
                }

        stage('deployment stage'){
                steps{
                        WithMaven('maven: maven3_5_3'){
                        sh 'mvn deploy'
                         }
                     }
                }
    }
}