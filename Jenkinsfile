node('master')
{
    stage ('continuousdownload-test')
    {
        git 'https://github.com/selenium-saikrishna/maven1.git'
    }
    stage ('continuousbuild-test')
    {
        sh 'mvn package'
    }
    stage ('continuousdeployment-test')
    {
        sh 'scp /home/ubuntu/.jenkins/workspace/pipe/webapp/target/webapp.war ubuntu@172.31.90.82:/var/lib/tomcat7/webapps/quen.war'
    }
    stage ('continuoustesting-test')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
    }
    stage ('continuousdelivery-test')
    {
        sh 'scp /home/ubuntu/.jenkins/workspace/pipe/webapp/target/webapp.war ubuntu@172.31.90.70:/var/lib/tomcat7/webapps/prod.war'
    }
}
  
  
  
  
  
  
  
  

