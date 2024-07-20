pipeline {
    agent any
   parameters{
       choice(name: 'VERSION', choices: ['1.10', '1.20', '1.30'], description: '')
        booleanParam (name: 'execute', defaultValue: true, description: '')
    }

    stages {
        stage('Build') {
          
            steps {
                echo 'Building the application'
               echo "building the version ${params.VERSION}" 
            }
        }
 stage('test') {
     when{
         expression{
             params.execute
         }
    }
    
            steps {
                echo 'testing the application'
            }
        }
 stage('Deploy') {
            steps {
                echo 'Deploy the application'
            }
        }

    }
}
