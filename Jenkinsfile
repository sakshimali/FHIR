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
bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=80526a6db8f45f25042fd4e156fa021cdb4e0488'
}
}

 

stage('Deploy Application to Mulesoft Cloudhub'){
steps{
bat 'mvn package deploy -DmuleDeploy'
}
}
}
}
