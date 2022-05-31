podTemplate(yaml: readTrusted('build-agent.yaml')) {
  node(POD_LABEL) { 
    stage('Build My Docker Image')  {
      steps {
        container('dind') {
            sh 'docker info'
            sh 'touch Dockerfile'
            sh 'echo "FROM centos:7" > Dockerfile'
            sh "cat Dockerfile"
            sh "docker -v"
            sh "docker info"
            sh "docker build -t my-centos:1 ."
        }
      }
    }
  }
}
