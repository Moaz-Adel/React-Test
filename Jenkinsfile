pipeline {

    stages {
        stage('build from a docker file new') {
            steps {
                script {
                    sh 'docker build -t moaz-adel/react-test -f Dockerfile.dev .'




                }


            }

        }
            stage('run those tests') {

                steps{

                     script {

                         env.DOCKER_BUILDKIT = 1
                         sh 'docker run -e CI=true moaz-adel/react-test npm run test'

                    }
                }

            }




    }
}