pipeline  {
  agent {lable 'Jenkins-agent6'}
  tool{
    jdk 'Java17'
    maven 'Maven3'
  }
  stages{
    stage {  "(Cleanup workspace")  
           steps {
             cleanws()
    }
    }
    stage  ("Check out from SCM"){
      steps {
        git branch: 'main',credentiolsid: 'github', url: 'https://github.com/pvreddy646/register-app'
    }
    }
    stage( "Build Application"){
      steps{
        sh "mvn cleanpackage"
        
    }
    }
    stage("Test application"){
      steps{
        sh "mvn test"
      }
    }
      
    }
  }
}
