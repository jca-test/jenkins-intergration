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
        stage('get build trigger'){
            if( env.CHANGE_BRANCH ){
                echo "is PR"
            }else if( env.TAG_NAME ){
                echo "tagged with ${env.TAG_NAME}"
            }else{
                echo "building ${env.BRANCH_NAME}"
            }
        }
    }
}
