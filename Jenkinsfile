
pipeline {
    
    agent any 
    
   stages {
        
        stage('Stage1_SP'){
           steps {
                echo 'This is the first stage'
           }
        }
        stage('Checkout_Stage2_Ranga'){
           steps {
               echo 'This is the second stage'
           }
        }
       stage('Checkout_Stage3_Saratrh'){
           steps {
               methodCall();
           }
        }
    }
}
