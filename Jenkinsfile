pipeline {
    agent any
    parameters{
        string (name:'Env',defaultValue:'Test',description:'version to deploy')
        booleanParam(name:'testexceution',defaultValue: true,description:'decide to run tc')
        choice(name: 'APPVERSION',choices:['1.1','1.2','1.3'])
    }
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
        stage('Deploy') {
            when{
                expression{
                    BRANCH_NAME == 'master'
                    }
                }
                steps{
                    script{
                        echo "deploying the app"
                        echo "deploying to env ${params.Env}"
                        echo "deploying the app version ${params.APPVERSION}"
                    }
               }
            }
        }   
    }
