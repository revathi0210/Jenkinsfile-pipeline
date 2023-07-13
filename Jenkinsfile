pipeline{
    
    tools{
        maven 'mymaven'
    }
    
    agent any
    
    stages{
        stage('Clone Repo'){
            steps{
                git 'https://github.com/revathi0210/DevOpsCodeDemo.git'
            }
        }
        
        stage('Complie Code'){
            steps{
                sh 'mvn compile'
                
            }
        }
        
        stage ('Code Review'){
            steps{
                sh 'mvn pmd:pmd'
                
            }
        }
        
        stage('Test code')
        {
            steps{
                sh 'mvn test'
            
            }
        }
        
        stage('Package Code')
        {
            steps{
                sh 'mvn package'
            }
        }
    }
}
