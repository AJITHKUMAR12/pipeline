pipeline {
    agent any
    parameters {
  //choice choices: ['1.10', '1.20', '1.30'], description: 'Select the version', name: 'VERSION'
  //booleanParam defaultValue: true, description: 'check and execute', name: 'check'
          choice(name: 'VERSION', choices: ['1.10', '1.20', '1.30'], description: 'select the version')
        booleanParam (name: 'execute', defaultValue: true, description: 'check and exceute')
}


    stages {
        stage('build') {
            when{
                expression{
                    params.execute
                }
            }
   
            steps {
                echo 'building the application'
            }
        }
    
   
        stage('test') {
   
            steps {
                echo 'testing the application'
                echo " the version for testing is ${params.VERSION}"
                
            }
        }
    

        stage('deploy') {
   
            steps {
                echo 'deploying the application'
            }
        }
    }
}
