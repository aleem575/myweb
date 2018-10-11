#! groovy
node{
 stage('Source'){
     git 'https://github.com/javahometech/myweb.git'
 }
 
 stage('Build'){
    // def mvnHome = tool 'maven2'
    sh "mvn clean package" 
 }
 stage('Send Email'){
     mail bcc: '', body: 'Demo Pipeline', cc: '', from: '', replyTo: '', subject: 'Pipeline Demo', to: 'aleem.shaik575@gmail.com'
 }
 stage('Archive'){
     archiveArtifacts 'target/*.war'
 }
}
