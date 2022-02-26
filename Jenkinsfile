pipeline {
    agent any
    enviroment {
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
                echo $APP_NAME
            }
        }
        stage("test"){
            steps {
                echo 'this is test step''
            }
        }
    }
}
