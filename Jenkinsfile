pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
         withCredentials([usernamePassword(credentialsId: 'mygit', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]){
            sh '''
              git config --global user.name $USERNAME
              git config --global user.email $USERNAME@gmail.com
              git clone https://$USERNAME:$PASSWORD@github.com/jerome-pir/test-multi.git
              git checkout $GIT_BRANCH
              cd test-multi
              cat values.yaml
            '''

            //build job: '../generic', parameters: [[$class: 'StringParameterValue', name: 'TEST', value: 'loick']]
         } 
            
         }
      }
   }
}
