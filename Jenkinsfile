node
{
def mavenHome = tool name : "maven3.9.6"

stage ('CheckoutCode')
{
git branch: 'master', git credentialsId: "5c348e0c-401f-4670-a27f-ade67cbf5422", url: "https://github.com/patilaboli23/maven-web-application.git"
}
stage ('Build')
{
sh "${mavenHome}/bin/mvn clean package"
}
/*
stage ('ExecuteSonarquebeReport')
{
sh "${mavenHome}/bin/mvn sonar:sonar"
}
stage ('UploadArtifactIntoNexas')
{
sh "${mavenHome}/bin/mvn deploy"
}
stage ('DeployIntoTomcat')
{
sshagent(['bbe74097-fb85-4ffd-9b33-97b363ea1de9'])
{
sh"scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.233.153.151:/opt/apache-tomcat-10.1.19/webapps/"
}
}
stage ('send EmailNotification')
{
emailext body: '''regards,
Aboli Patil.''', subject: 'Bild is completed', to: 'patilaboli23@gmail.com'
}
*/

}
