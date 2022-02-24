node{
  stage('SCM CHECKOUT'){
    sh 'git init'
    git 'https://github.com/Samarjeet0007/Jenkinsfile-git-maven-project'
  }
  stage('COMPILE & PACKAGE'){
    sh 'mvn package'
  }
}
