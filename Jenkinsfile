pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
            build job: 'generic', parameters: [[$class: 'StringParameterValue', name: 'TEST', value: 'loick']]
         }
      }
   }
}
