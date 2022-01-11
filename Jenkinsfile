pipeline {
    agent any
    parameters{
        string (name:'Env',defaultvalue:'Test',description:'version to deploy')
        booleanParam(name:'testexceution',defaultversion: true,description:'decide to run tc')
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
            when{
                expression{
                    params.executeTests == true 
                }
            }
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
        stage('deploy') {
            steps {
                script{
                    echo "deploying the app"
                    echo "deploying to env ${params.Env}"
                    echo "deploying the app version ${params.APPVERSION}"

                }
            }
        }
    }   
}
