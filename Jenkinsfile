pipeline{
  agent any
  stages{
    stage("Build docker Image"){
      steps{
        echo 'Building Docker Image'
        sh 'sudo docker build -t my-python-app .'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deploying'
        sh 'sudo docker run -d -p 5000:5000 my-python-app'
      }
    }
  }
}
