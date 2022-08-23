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
       state= "$state"
     }
     
  stages {
      
     
    stage('Some step') {
        when { expression { env.state == 'open' } } 
     
      steps {
        
        sh '''#!/bin/bash
        echo Start-Pipeline 
        echo $ref
        
        '''
        //  sh test1.sh
  // sh /home/jenkins/test1.sh   
        
      }
    }
  }
}
