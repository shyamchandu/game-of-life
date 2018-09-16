node {
    stage('GitStage') {
    git 'https://github.com/wakaleo/game-of-life.git'
}

 stage('Build & Package') {
    sh 'mvn package'
}

 stage('Results') {
    archiveArtifacts 'gameoflife-web/target/gameoflife.war'
    junit 'gameoflife-web/target/surefire-reports/*.xml'
}

}
