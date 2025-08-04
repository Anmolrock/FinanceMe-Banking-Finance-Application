pipeline{
    
    agent any
    
    tools{
        maven 'mymaven'
    }
    
    stages{
        stage('Clone Repo')
        {
            steps{
                git 'https://github.com/Anmolrock/FinanceMe-Banking-Finance-Application.git'
            }
        }
        stage('Test Code')
        {
            steps{
                sh 'mvn test'
            }
        }
        
        stage('Build Code')
        {
            steps{
                sh 'mvn package'
            }
        }
        stage('Build Image')
        {
            steps{
                sh 'docker build -t myproject1:$BUILD_NUMBER .'
            }
        }
        
        stage('Deploy the Image')
        {
            steps{
                sh 'docker run -d -P myproject1:$BUILD_NUMBER '
            }
        }
    }
}
