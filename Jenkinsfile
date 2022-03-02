pipeline {
    agent any
    environment{
        APP_NAME = 'Hello World'   
    }
    parameters {
        text('name': 'my_text', defaultValue: 'hello world', description: 'this is text param')
        string('name': 'my_string', defaultValue: 'this is string', description: 'this is tring param')
        booleanParam('name': 'my_boolean', defaultValue: false, description: 'this is boolean param')
        choice('name': 'my_choice', choices: ['money', 'game'], description: 'this is choices param')
        password('name': 'my_password', defaultValue: 'mypass', description: 'this is password pararm')
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    }
    stages {
        stage("build"){
            
            when {
                expression {
                    BRANCH_NAME == 'main'   
                }
            }
            parallel {
                stage('build a'){
                    steps {
                        script {
                            def cur_date = new Date()   
                        }
                        echo "build aaaaaaa at ${cur_date}"
                    }
                }
                stage('build b'){
                    steps {
                        script {
                            def cur_date = new Date()   
                        }
                        echo "build bbbbbbbbbbb at ${cur_date}"
                    }
                }
            }
        }
        stage("test"){
            steps {
                echo "this is test step ${APP_NAME}"
                echo "Hello ${params.PERSON}"
            }
        }
    }
}
