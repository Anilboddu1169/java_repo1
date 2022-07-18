pipeline {
    agent {
  label 'tomcat-slav2'
}
stages {
  stage('git checkout') {
    steps {
      git 'https://github.com/Anilboddu1169/java_repo1.git'
    }
  }

  stage('build') {
    steps {
      sh 'mvn clean install'
    }
  }

  stage('push to artifactory') {
    parallel {
  stage('push to artifactory1') {
steps {
     sleep 15
    }
}
stage('push to artifactory2') {
steps {
     sleep 15
    }
  }
}
}

  stage('deploy') {
    steps {
      sh 'sudo cp /home/ec2-user/jenkins-slav2/workspace/proj2-parallel/target/*.war /opt/apache-tomcat-9.0.64/webapps/'
    }
  }

}
}
