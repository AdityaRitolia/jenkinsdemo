pipeline{
  agent any
  stages{
    stage("Clean up"){
      steps{
        deleteDir();
      }
    }
    stage("Clone Repo"){
      steps{
        sh "git clone https://github.com/AdityaRitolia/jenkinsdemo.git"
      }
    }
    stage("Build"){
      dir("jenkinsdemo")
      sh "clean install"
    }
    stage("Test"){
      dir("jenkinsdemo")
      sh "test"
    }
  }
}
