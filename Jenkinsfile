pipeline {
  agent any

  stages {
    stage('Checkout Code') {
      steps {
        checkout scm
      }
    }

    stage('Build React App') {
      agent {
        docker {
          image 'node:18'
          args '-u root'  
        }
      }
      steps {
        sh 'npm install'
        sh 'npm run build'
        sh 'cp -r dist dist_for_deploy'  
      }
    }

  stage('Deploy Build') {
  agent {
    docker {
      image 'node:18'
      args '-v /home/<user>/jenkins-react-deploy:/usr/share/nginx/html -u root' // replace <user> with your Linux username.
    }
  }
  steps {
    sh """
      rm -rf /usr/share/nginx/html/*
      cp -r dist_for_deploy/* /usr/share/nginx/html/
    """
  }
}
  }
}
