pipeline
{
agent any
stages{
stage('Build Application'){
steps{
bat 'mvn clean install'
}

}

 

stage('SonarQube Testing'){
steps{
bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=22e860b514c161fdd1223a2cd693139452d57a06'
}
}

 

stage('Deploy Application to Mulesoft Cloudhub'){
steps{
bat 'mvn package deploy -DmuleDeploy'
}
}
}
}
