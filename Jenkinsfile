pipeline {

  agent any
  
  stages {
    
    stage("build") {
    
      steps {
        echo 'Starting building the App'
      }
    }
    
    stage("test") {
    
      steps {
        input('Continue ?')
      }
    }
    
    stage("deploy") {
      parallel {
        stage('Deploy start ') {
          steps {
            echo "Start the deploy..."
          }
        }
        
     stage('Deploying now') {
       agent {
         docker {
           reuseNode true
           image 'nginx'
         }
       }
       
        steps {
          echo 'Created'
        }
    }
  }
}
