pipeline  {
  agent {lable 'Jenkins-agent'}
  tools{
    jdk 'Java17'
    maven 'Maven3'
  }
  stages{
    stage   ("Cleanup workspace"){  
           steps {
           cleanws()
           }
    }
    
    stage("Checkout from SCM"){
      steps {
        git branch: 'main',credentialsid: 'github', url: 'https://github.com/pvreddy646/register-app'
      }
    }
    
    stage( "Build Application"){
      steps{
        sh "mvn clean package"
      }

    }
    
    stage("Test application"){
      steps{
        sh "mvn test"
      }  
    }
  }  
} 
  

