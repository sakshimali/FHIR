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
bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=a421a9e4a578e65d84eb26b5c84421ca41847f2e'
}
}

 

stage('Deploy Application to Mulesoft Cloudhub'){
steps{
bat 'mvn package deploy -DmuleDeploy'
}
}

 

}
}