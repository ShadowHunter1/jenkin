pipeline {
    agent any
    environment{
        APP_NAME = 'Hello World'   
    }
    stages {
        stage("build"){
            when {
                expression {
                    BRANCH_NAME == 'develop'   
                }
            }
            steps {
                echo 'this is build step'
                echo "this is ${APP_NAME} app"
            }
        }
        stage("test"){
            steps {
                echo 'this is test step ${APP_NAME}'
            }
        }
    }
}
