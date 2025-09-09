pipeline {
    agent any

    environment {

        GIT_CREDENTIALS_ID = '	github-cred' // Jenkins me save kiya hua GitHub credentials ka ID
        REPO_URL = 'https://github.com/muhammadfurqannasir/intro.git'
        BRANCH = 'main'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: "${BRANCH}", credentialsId: "${GIT_CREDENTIALS_ID}", url: "${REPO_URL}"
            }
        }

        
        stage('Commit & Push Changes') {
            steps {
                bat '''

                    git config --global user.email "muhammadfurqannasir3@gmail.com"
                    git config --global user.name "Muhammad Furqan Nasir"
                    git add .
                    git commit -m "Automated build from Jenkins" || exit 0
                    git push origin %BRANCH%

                '''
            }
        }
    }
}
