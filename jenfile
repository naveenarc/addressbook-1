pipeline {
    agent any

    stages {
        stage('Compiler3') {
            steps {
                script{
                    echo "compiling the code"
                }
            }
        }
        stage('unittest') {
            steps {
                script{
                    echo "Testing the code"
                }
            }
       }
        stage('packagejob') {
            steps {
                script{
                    echo "Packaging the code"
                }
            }
        }
    }   
}
