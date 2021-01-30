node{
stage('git checkout')
{
git 'https://github.com/NaruPraveenKumar/Hello'
}
stage('build a package')
{
 def maven=tool name: 'Maven', type: 'maven'
  sh "{{$maven}}/bin/mvn clean package"
}
}
