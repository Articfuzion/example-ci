pipeline {
agent any
stages {
stage(’Build’) {
steps {
sh ’ls’
}
}
}
post {
always {
archiveArtifacts artifacts: ’tar cfz website.tgz _less.github.io’,
fingerprint: true
}
}
}
