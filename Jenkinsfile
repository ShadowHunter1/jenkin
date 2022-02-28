pipeline {
    agent any
    environment{
        APP_NAME = 'Hello World'   
    }
    parameters {
        text('name': 'my_text', defaultValue: 'hello world', description: 'this is text param')
        string('name': 'my_string', defaultValue: 'this is string', description: 'this is tring param')
        booleanPararm('name': 'my_boolean', defaultValue: false, description: 'this is boolean param')
        choice('name': 'my_choice', choices: ['money', 'game'], description: 'this is choices param')
        password('name': 'my_password', defaultValue: 'mypass', description: 'this is password pararm')
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
                echo "this is test step ${APP_NAME}"
                echo "this is my_text pararm ${pararms.my_text}"
            }
        }
    }
}
