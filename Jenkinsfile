

pipeline {
    agent any //run on any jenkins available node or where to execute
    
    stages { //where whole work actual happens
        stage("build") {
        
            steps { //which will executein jenkins server
                   
                   echo 'building the application.......... '
                   
               }
        }
        stage("test") {
        
            steps {
            
                  echo 'testing the application....... '
                  
            }
        }
        stage("deploy") {
        
            steps {
            
                echo 'deploying the application........ '
            }
        }
    }   
}
