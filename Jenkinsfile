pipeline {
  agent {
           label 'Jenkins-Master'
         }
   triggers {
    GenericTrigger(
     genericVariables: [
      [key: 'ref', value: '$.pull_request.head.ref'],
      [key: 'state', value: '$.pull_request.state']
     ],
    
    token: '148946516123',
    tokenCredentialId: ''
      
    )
   }
   environment{ 
       state1= "$state"
     }
     
  stages {
      
     
    stage('Some step') {
         when { expression { env.state1 == 'open' } } 
     
      steps {
        
        sh '''#!/bin/bash
        echo $state1
        
        
        '''
        //  sh test1.sh
  // sh /home/jenkins/test1.sh   
        
      }
    }
  }
}
