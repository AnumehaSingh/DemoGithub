

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
        stage('Tests') {
                parallel(
                    'Unit Tests': {
                        container('node') {
                            sh("npm test --cat=unit")
                        }
                    },
                    'API Tests': {
                        container('node') {
                            sh("npm test --cat=acceptance")
                        }
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
