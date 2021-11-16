pipeline {
  
  agent any
  
    stages {
  
        stage('build') {
    
             steps {
      
                 echo 'builing main again'
                 echo 'builing newbranch1'
                 checkout([$class: 'GitSCM', branches: [[name: '*/multibranch-sample1']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/zubairRiyaz/multibranch-pipeline-demo.git']]])
             }
        }
    
        stage('test') {
    
             steps {
                 echo 'testing shell'
                 sh "chmod +x -R ${env.WORKSPACE}"
                 sh './test/shell.sh'
             }
        }
    
  
        stage('deploy') {
    
             steps {
                 echo 'deploying main'
             }
        }
    }
}
