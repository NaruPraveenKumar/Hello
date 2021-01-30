node{
stage('git checkout')
{
git 'https://github.com/NaruPraveenKumar/Hello'
}
stage('build a package')
{
 def maven = tool name: 'Maven', type: 'maven'
 sh "${maven}/bin/mvn clean package"
}
 stage('sending an email')
 {
  mail bcc: '', body: '''Hi ,

Jenkin job is running.

Thanks,
Praveen''', cc: 'praveenit.naru@gmail.com', from: '', replyTo: '', subject: 'Jenkins job info', to: 'praveen1993.naru@gmail.com'
 }
}
