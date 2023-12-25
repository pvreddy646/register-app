pipeline  {
  agent {label 'Jenkins-agent'}
  tools{
     jdk 'java17'
    maven 'maven3'
  }
  stages{
    stage("Cleanup workspace"){  
           steps {
           cleanWs()
           }
    }
    
    stage("Checkout from SCM"){
      steps {
          git branch: 'main', credentialsId: 'github', url: 'https://github.com/pvreddy646/register-app'
        }
    }
    
    stage("Build Application"){
        steps {
            sh "mvn clean package"
       }

  }
    
    stage("Test Application"){
      steps{
        sh "mvn test"
       }  
    }
  }  
} 
  

