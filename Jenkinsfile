pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Add your build steps here
                // This could include compiling code, running tests, etc.
            }
        }

        stage('Deploy') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'infinitefree-credentials',
                        usernameVariable: 'if0_34524946',
                        passwordVariable: '6Rwt0Sz3inwgag'
                    )
                ]) {
                    sh "scp -r * ${env.if0_34524946}@example1.000.pe:/htdocs/"
                }

                // Additional deployment steps, if needed
                // ...
            }
        }
    }
}
