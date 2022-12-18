pipeline{
  agent{
    label 'AlderlakeAgent'
  }
  stages{
  stage('Pull')
    {
      steps{
       git branch: 'main', url: 'https://github.com/ajinkyagitrepo/WebsiteusingReactJS.git'
      }
    }
    stage('Build')
    {
      steps{
       sh 'npm install'
      }
    }
    stage('Deploy')
    {
      steps{
      sh 'npm start'
      }
  }
  }
    post{
      success{
    echo 'THIS IS A POST STEP YOUR DEPLOYMENT IS COMPLETED'
      }
    }
}
