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
  
  
//   environment{
//     ref=123
 //  }
  stages {
    stage('Some step') {
      steps {
        sshagent (credentials: ['Docker-Server-Test']) {
        
        sh '''
        ssh docker@10.33.133.100 "cd /home/docker
        env ref=$ref sh test1.sh"
        
        
        '''
        //  sh test1.sh
  // sh /home/jenkins/test1.sh   
        }
      }
    }
  }
}
