pipeline {
 agent any
  tools {
maven 'Maven'
    jdk 'jdk'
  }
  stages {
stage('Checkout'){
steps {
git branch:'master', url:'https://github.com/RachanaN-27/1bi23cs162_finaltest.git'
}
}
    stage('Build') {
steps {
sh 'mvn clean package'
}
    }
    stage('Test') {
steps {
sh 'mvn test'
}
    }
    stage('Run Application') {
steps {
sh 'java -jar target/1bi23cs162-finaltest-1.0-SNAPSHOT.jar'
}
    }
  }
  post {
success{
echo "Build suceessful"
}
    failure {
echo "Build failure"
    }
  }
}
