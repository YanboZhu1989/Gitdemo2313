pipieline {
    agent any

    stage {
        stage("build") {
            step {
                echo 'building the application'
            }
        }
    }

    stage {
        stage("test") {
            when{
                expression{
                    BRANCH_NAME == 'dev' ||  BRANCH_NAME == 'master'
                }
            }
            step{
                echo 'testing the application'
        }
    }

    }

    stage {
        stage("deploy") {
            step{
                echo 'deploying the application'
            }
        }
    }
    post {
        always {
            echo 'hello world'        }
        
    }
}
