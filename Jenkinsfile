pipeline {
    agent any
    parameters {
  choice choices: ['1.20,1.30,1.40'], description: 'Select the version', name: 'VERSION'
  booleanParam defaultValue: true, description: 'check and execute', name: 'excute'
}


    stages {
        stage('build') {
            when{
                expression{
                    params.excute
                }
            }
   
            steps {
                echo 'building the application'
            }
        }
    }
    stages {
        stage('test') {
   
            steps {
                echo 'testing the application'
                echo " the version for testing is $(params.VERSION)"
            }
        }
    }
    stages {
        stage('deploy') {
   
            steps {
                echo 'deploying the application'
            }
        }
    }
}
