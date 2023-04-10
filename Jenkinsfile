pipeline {
    agent{
        label 'controller'
    }
    triggers{
        pollSCM ('*****')
    } 
    //agent none 
    stages{
        stage ('Compile'){
            agent{
                label 'controller'
            }
            steps {
                echo "Compiling the Code"
                sh './mvnw compile'
            }
        }
        stage ('Unit Test'){
            agent{
                label 'controller'
            }
            steps {
                echo "Testing the code by a Unit Test"
                //sh './mvnw test'
            }
        }
        stage ('Code Quality Test'){
            agent{
                label 'controller'
            }
            steps {
                echo "Code coverate and static code analysis"
            }
        }
    }
}
