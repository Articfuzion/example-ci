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
archiveArtifacts artefacts: ’tar cfz website.tgz _less.github.io’,
fingerprint: true
}
}
}
