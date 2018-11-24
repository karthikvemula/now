node('master')
{
    stage ('continuousdownload-master')
    {
        git 'https://github.com/selenium-saikrishna/maven1.git'
    }
    stage ('continuousbuild-master')
    {
        sh 'mvn package'
    }
    stage ('continuousdeployment-master')
    {
        sh 'scp /home/ubuntu/.jenkins/workspace/pipe/webapp/target/webapp.war ubuntu@172.31.90.82:/var/lib/tomcat7/webapps/quen.war'
    }
    stage ('continuoustesting-master')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
    }
    stage ('continuousdelivery-master')
    {
        sh 'scp /home/ubuntu/.jenkins/workspace/pipe/webapp/target/webapp.war ubuntu@172.31.90.70:/var/lib/tomcat7/webapps/prod.war'
    }
}
  
  
  
  
  
  
  
  

