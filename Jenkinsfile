@Library('piper-lib-os') _

node() {
    stage('init') {
        deleteDir()
        checkout scm
    }
    stage('Integration Artifact Download Command') {
        integrationArtifactDownload script: this
    }
}
