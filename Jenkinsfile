pipeline {
    agent any
    stages {
        stage('deploy') {
            steps {
              sh "/var/jenkins_home/./aws/dist/aws configure set region $AWS_DEFAULT_REGION" 
              sh "/var/jenkins_home/./aws/dist/aws configure set aws_access_key_id $AWS_ACCESS_KEY_ID"  
              sh "/var/jenkins_home/./aws/dist/aws configure set aws_secret_access_key $AWS_SECRET_ACCESS_KEY"
              sh "/var/jenkins_home/./aws/dist/aws s3 cp --recursive src/ s3://ruwanthi"
            }
        }
    }
}
