pipeline {
    //hi
    
    agent {
        label 'docker'
    }

    stages {
        stage('build from a docker file new') {
            steps {
                script {
                    sh 'docker build -t Moaz-Adel/React-Test -f Dockerfile.dev .'




                }


            }

        }
            stage('run those tests') {

                steps{

                     script {

                         env.DOCKER_BUILDKIT = 1
                         sh 'docker run -e CI=true Moaz-Adel/React-Test npm run test'

                    }
                }

            }




    }



}