pipeline{
agent any
tools{
    maven 'MAVEN'
}
stages{
    stage("Build Maven"){
        steps{
checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'git', url: 'https://github.com/aliyevom/dev']])
        sh "mvn -Dmaven.test.failure.ignore=true clean package"
        }

    }
}

}




















