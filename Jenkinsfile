pipeline {
    agent any

    stages {
        stage("build") {
            steps {
                echo 'building the application'
            }
        }
    }

    stages {
        stage("test") {
            when{
                expression{
                    BRANCH_NAME == 'dev' ||  BRANCH_NAME == 'master'
                }
            }
            steps {
                echo 'testing the application'
        }
    }

    }

    stages {
        stage("deploy") {
            steps {
                echo 'deploying the application'
            }
        }
    }
    post {
        always {
            echo 'hello world'        }
        
    }
}
