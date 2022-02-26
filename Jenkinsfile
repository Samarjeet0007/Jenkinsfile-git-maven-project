node{
  stage('SCM CHECKOUT'){
    git url: 'https://github.com/Samarjeet0007/Jenkinsfile-git-maven-project', branch: 'main'
  }
  stage('COMPILE & PACKAGE'){
    def mvn_home = tool name: 'maven_1', type: 'maven'
    sh "${mvn_home}/bin/mvn package"
  }
  stage('Email Notification'){
     //first configure jenkins -> SMTP server setup -> smtp.gamil.com(email_server)
    /*
      mail bcc: '', body: '''Hello There,

Jenkins Update...

Thank you,
Jenkins_Admin''', cc: '', from: '', replyTo: '', subject: 'Jenkins_update', to: 'samarjeetkumar9662@gmail.com'
    */
    echo "Skipping for now!"
  }
}
