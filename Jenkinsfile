pipeline {
    agent any
     stages{
            stage("Scm checkout"){
                steps{
                echo "git code checked out";
                git credentialsId: 'fe5aa3f7-201c-45c8-9003-84fa85976dcb', url: 'https://github.com/hamsyed/HelloWorld.git'
                }
            }
            stage("compile and build and test"){
                steps{
                echo "code is successsfully build";
                
                }
            }
            stage("Deploy"){
                steps{
                    echo "Deploy Pass";
                }
            }
        }
    
    
    post {
        always{
            echo "always run this"
        }
        success{
            echo "deployment is scuccessfull"
        }
        failure {
            echo "failed"
        }
        unstable{
            echo "unstable build"
            
        }
        changed{
            echo "pipeline changed"
        }
    }
 }
