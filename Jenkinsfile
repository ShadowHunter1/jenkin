pipeline {
    agent any
    stages {
        stage("build"){
            when {
                expression {
                    BRANCH_NAME == 'develop'   
                }
            }
            steps {
                echo 'this is build step'
            }
        }
        stage("test"){
            steps {
                echo 'this is test step''
            }
        }
    }
}
