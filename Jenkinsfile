pipeline{

    agent any

    stages{

        stage('cean repo'){

            steps{

                sh "mvn clean"

            }

        }

        stage ('test'){

            steps {

                sh "mvn test"

            }

        }

        stage ('package'){

            steps {

                sh "mvn compile"

            }

        }
        
        stage ('install'){

            steps{

                sh "mvn install"

            }

        }

        stage ('deploy'){

            steps{

                sh "cp /root/.jenkins/workspace/pipelinetest/target/newproj.war /opt/apache-tomcat-9.0.29/webapps"

            }

        }

    }

}
