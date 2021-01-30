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
  emailext body: '''Hi  Team,
Jenkins job is running please be careful .

Thanks,
Praveen''', subject: 'About jenkins', to: 'praveen1993.naru@gmail.com'
 }
}
