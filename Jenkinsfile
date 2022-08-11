pipeline {
  agent {
           label 'Jenkins-Master'
         }
   triggers {
    GenericTrigger(
     genericVariables: [
      [key: 'ref', value: '$.pull_request.head.ref']
     ],
    
    token: '148946516123',
    tokenCredentialId: ''
      
  )
 }
  
 environment{
        ref='$ref'

  } 
  
  stages {
    stage('Some step') {
      steps {
        sh '''
        echo "${env.ref}"
        sh "/home/jenkins/test1.sh"      
        '''
      }
    }
  }
}
