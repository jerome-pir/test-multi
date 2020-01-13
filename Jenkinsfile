pipeline {
   agent any

   stages {
      stage('Hello') {
        steps {
         checkout scm
            sh '''
              cat values.yaml
            '''
            //build job: '../generic', parameters: [[$class: 'StringParameterValue', name: 'TEST', value: 'loick']]
         }

      }
   }
}
