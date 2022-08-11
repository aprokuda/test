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
  
  stages {
    stage('Some step') {
      steps {
        sh '''
        sh /home/jenkins/test1.sh      
        '''
      }
    }
  }
}
