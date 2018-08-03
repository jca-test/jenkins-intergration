throttle(['docker']) {
    node('docker') {
        stage('Set up') {
            checkout scm
        }

        stage('Docker Build'){
            sh """
                echo "ok"
            """
        }
        stage('env'){
            sh """
                env
            """
        }
    }
}
