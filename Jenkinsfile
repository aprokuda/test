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
        ssh docker@10.33.133.100 'cd /home/docker
        sh test1.sh'
        
          
        '''
  // sh /home/jenkins/test1.sh   
      }
    }
  }
}
