pipeline {
    //hi again
    
    agent {
        label 'docker'
    }

    stages {
        stage('build from a docker file new') {
            steps {
                script {
                    sh 'docker build -t moaz-adel/testing -f Dockerfile.dev .'




                }


            }

        }
            stage('run those tests') {

                steps{

                     script {

                         env.DOCKER_BUILDKIT = 1
                         sh 'docker run -e CI=true moaz-adel/testing npm run test'

                    }
                }

            }




    }



}