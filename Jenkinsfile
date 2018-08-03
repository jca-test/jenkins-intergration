throttle(['docker']) {
    node('docker') {
        stage('Set up') {
            def scmVars = checkout scm
            def commitHash = scmVars.GIT_COMMIT
            for (scmVar in scmVars){
                echo "scmVar $scmVar"
            }
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
