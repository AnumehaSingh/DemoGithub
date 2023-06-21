

pipeline {
    agent { //run on any jenkins available node or where to execute
        label 'Sel-Windows'
    } 
    parameters {
        string(name: 'IIP', description: 'IIP run')
        string(name: 'APIM', description: 'APIM run')
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
                            
                             echo 'building first task the application.......... '
                        },
                        "secondTask" : {
                             echo 'building second task the application.......... '
                        }
                    )
                }
            }
          stage('QA') {
    when { expression { params.CLICK == 'QA' } }
      steps {
        script {
           CHOICES = ['IIP', 'APIM', 'STUDIO'];    
                    env.CLICK1 = input  message: 'Choose appropriate Test?',ok : 'Deploy',id :'tag_id', parameters:[choice(choices: CHOICES, description: 'Make a choice', name: 'Select')]
                } 

            }
    }  
    parallel {
        stage('A') {
            when {
                expression { env.CLICK == 'IIP' }
            }
            steps {
              echo "A"
            } 
        }
        stage('B') {
            when {
                expression { env.CLICK == 'APIM' }
            }
            steps {
              echo "B"
            } 
        }
        stage('C') {
            when {
                expression { env.CLICK == 'STUDIO' }
            }
            steps {
              echo "C"
            } 
        }
    }
  }
}
        stage("deploy") {
        
            steps {
            
                echo 'deploying the application........ '
            }
        }
    }   
}
