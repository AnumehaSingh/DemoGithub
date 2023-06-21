

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
            stage("Parallel") {
                steps {
                    parallel (
                        "firstTask" : {
                            //do some stuff
                        },
                        "secondTask" : {
                            // Do some other stuff in parallel
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
