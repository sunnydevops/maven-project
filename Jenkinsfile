node{

    stage('SCM'){
        git 'https://github.com/sunnydevops/maven-project.git'

    }

    stage('Build & Package'){
        def mvnHome = tool name: 'maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }

    stage('artifactory'){
        archiveArtifacts 'Gameoflife-pipeline/webapp/target/webapp.war'
    }

    
}