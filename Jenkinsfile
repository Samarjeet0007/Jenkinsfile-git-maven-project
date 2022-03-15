/*
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
    *//*
      mail bcc: '', body: '''Hello There,

Jenkins Update...

Thank you,
Jenkins_Admin''', cc: '', from: '', replyTo: '', subject: 'Jenkins_update', to: 'samarjeetkumar9662@gmail.com'
    *//*
    echo "Skipping for now!"
  }
}
*/
/*
sshagent(['ec2_instance_key']) {
    sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@54.234.14.47:/var/lib/tomcat/webapps'
}
*/



/*
pipeline{
    agent any
    
    tools {
        maven 'maven_1'
    }
    
    environment {
        docker_tag = getVersion()
    }
    stages{
        stage('SCM CHECKOUT'){
            steps{
                git url: 'https://github.com/Samarjeet0007/Jenkinsfile-git-maven-project', 
                branch: 'main'
            }
        }
        stage('MVN BUILD'){
            steps{
                //def MVN_HOME = tool name: 'maven_1', type: 'maven'
                sh "mvn clean package"
            } 
        }
        stage('DOCKER BUILD'){
            steps{
                sh "docker build . -t 996622/warfromjenkins:${docker_tag}"
            }
        }
        stage('DOCKER PUSH'){
            steps{
                withCredentials([string(credentialsId: 'docker-pass', variable: 'dockerpass')]) {
                sh "docker login -u 996622 -p ${dockerpass}"
                }
                sh "docker push 996622/warfromjenkins:${docker_tag}"
            }
        }
        stage('ANSIBLE_to_DEPLOY_CONTAINER'){
            steps{
                ansiblePlaybook colorized: true, credentialsId: 'ec2_instance_key', 
                disableHostKeyChecking: true, extras: "-e docker_tag=${docker_tag}", installation: 'ansible_', 
                inventory: 'hosts.ini', playbook: 'docker-container-playbook'
            }
        }
    }
}

def getVersion(){
    def getuniqe = sh returnStdout: true, script: 'echo $RANDOM'
    return getuniqe
}
*/



node{
  stage('one'){
     echo "executing in multi-branch"
  }
}
