

pipeline {
    agent { //run on any jenkins available node or where to execute
        label 'Sel-Windows'
    } 
    
    stages { //where whole work actual happens
        stage("build") {
        
            steps { //which will be execute in jenkins server
                   
                   echo 'building the application.......... '
                   
               }
        }
        stage("test") {
        
           parallel(
                    'Unit Tests': {
                                     echo 'Unit Tests for building the application.......... '
                },
                    'API Tests': {
                                    echo 'API Tests for building the application.......... '
            }
        )

    }
        stage("deploy") {
        
            steps {
            
                echo 'deploying the application........ '
            }
        }
    }   
}
