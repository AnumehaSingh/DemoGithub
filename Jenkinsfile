

pipeline {
    agent { //run on any jenkins available node or where to execute
        label 'Sel-Windows'
    } 
     parameters {
          string(name: 'SYSTEM', defaultValue: '', description: 'Enter array. Example:SYS-123')

          string(name: 'EMail', defaultValue: '', description: 'Enter email id')
 }
    
    stages { //where whole work actual happens
        stage("build") {
        
            steps { //which will be execute in jenkins server
                   
                   echo 'building the application.......... '
                   
               }
        }
            stage("Parallel") {
                steps {
                    parallel (
                        stage('A'){
                             echo 'building first task the application.......... '
                        },
                        stage('B'){
                             echo 'building second task the application.......... '
                        }
                    )
                }
            }
        stage("deploy") {
        
            steps {
            
                echo 'deploying the application........ '
            }
        }
    }   
}
