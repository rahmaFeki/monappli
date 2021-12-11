pipeline{
  agent any
  tools { maven 'Maven' }
  stages{
    stage("Delete workspace"){
      steps{
        cleanWs deleteDirs:true
        checkout scm
      }
    }
    stage("Build monappli"){
        steps{
        bat ''' mvn clean install '''
        }
     }
  }
}
