pipeline {
agent any
stages {
stage(’Build’) {
steps {
  sh 'npm install'
  sh 'npm install grunt-cli'
  sh './node_modules/grunt-cli/bin/grunt'
}
}
  stage('Archive'){
    steps{
      sh 'tar cfz website.tgz _less.github.io'
    }
  }
  
}
post {
always {
archiveArtifacts artifacts: ’website.tgz’, fingerprint: true
}
}
}
