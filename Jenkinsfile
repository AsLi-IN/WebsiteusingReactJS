pipeline{
  agent{
    label 'AlderlakeAgent'
  }
  stages{
  stage('Pull')
    {
      steps{
       git 'https://github.com/ajinkyagitrepo/WebsiteusingReactJS.git'
      }
    }
    stage('Build')
    {
      steps{
       npm install 
      }
    }
    stage('Deploy')
    {
      steps{
       npm start 
      }
  }
    post{
      success{
    echo "THIS IS A POST STEP YOUR DEPLOYMENT IS COMPLETED"
      }
    }
}
