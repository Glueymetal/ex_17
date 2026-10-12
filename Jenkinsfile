pipeline{
    agent any
    stages{
        stage('Checkout')
        {
            steps{
                checkout scm
            }
        }
        stage('Build'){
            steps{
                echo "Building branch ${env.BRANCH_NAME}"
            }
        }
        stage('Test')[
            steps{
                echo "Running Tests on  ${env.BRANCH_NAME}" 
            }
        ]
        stage('Deploy')
        {
            when {branch 'main'}
            steps {echo 'Deploying from main only'}
        }
    }
}