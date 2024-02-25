jenkins shared library 
===============

@Library("your-shared-library") _    <<<<--- use this syntax in jenkinsfile when you are using shared libraries


"your-shared-library" must be declared or defined in global pipeline libraries (manage jenkins->configure system->global pipeline libraries)


shared libraries file must be in vars folder.. whether it may be in separate repo or in same repo where jenkinsfile exists 


in vars folder, create shared library(functionCall.groovy) as below. 

def call() {
  sh 'echo Hi This is the output from fucall.groovy'
}
 

Example Jenkinsfile
--------------------

@Library("your-shared-library") _

pipeline {
    
    agent any 
    
   stages {
        
        stage('Stage1_SP'){
           steps {
                echo 'Hello Deops Siva prasad'
           }
        }
        stage('Checkout_Stage2_Ranga'){
           steps {
                functionCall()
           }
        }
    }
}
