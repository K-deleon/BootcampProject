@Library('piper-lib-os') _

node() {
        stage('Checkout') {
            steps {
                script {
                    // Configure Git to use sparse checkout
                    checkout([$class: 'GitSCM',
                        branches: [[name: '*/master']],
                        doGenerateSubmoduleConfigurations: false,
                        extensions: [[$class: 'SparseCheckoutPaths', sparseCheckoutPaths: [[path: 'downloads']]]],
                        submoduleCfg: [],
                        userRemoteConfigs: [[url: 'https://github.com/K-deleon/BootcampProject.git']]])
                    
                    // Print the workspace path
                    echo "Workspace path: ${workspace}"
                }
            }
        }
}
