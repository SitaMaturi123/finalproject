pipeline {
  agent {
    docker {
      image 'abhishekf5/maven-abhishek-docker-agent:v1'
      args '--user root -v /var/run/docker.sock:/var/run/docker.sock' // mount Docker socket to access the host's Docker daemon
  }
}
  stages {
    stage('check out') {
      steps {
        sh 'echo passed'
      }
    }
  }
  stage('build and test') {
  steps {
    sh 'ls -ltr'
    sh 'cd java-maven-sonar-argocd-helm-k8s/spring-boot-app && mvn clean package'
  }
}
}

