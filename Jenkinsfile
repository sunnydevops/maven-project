node{

    stage('SCM'){
        git 'https://github.com/sunnydevops/maven-project.git'

    }

    stage('Build & Package'){
        tool name: 'maven', type: 'maven'
    }

    stage('artifactory'){
        archiveArtifacts 'gameoflife-web/target/gameoflife.war'
    }

    stage('Junit'){
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}