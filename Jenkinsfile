pipeline {
    agent any

    environment {
<<<<<<< HEAD
        GIT_CREDENTIALS_ID = '	github-token' // Jenkins me save kiya hua GitHub credentials ka ID
        REPO_URL = 'https://github.com/jaweria15/intro.git'
=======
        GIT_CREDENTIALS_ID = '	github-cred' // Jenkins me save kiya hua GitHub credentials ka ID
        REPO_URL = 'https://github.com/muhammadfurqannasir/intro.git'
>>>>>>> ff46a782584ce68197025661a127ab334b00f586
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
<<<<<<< HEAD
                    git config --global user.email "javeriaf322@gmail.com"
                    git config --global user.name "Jaweria"
=======
                    git config --global user.email "muhammadfurqannasir3@gmail.com"
                    git config --global user.name "Muhammad Furqan Nasir"
>>>>>>> ff46a782584ce68197025661a127ab334b00f586
                    git add .
                    git commit -m "Automated build from Jenkins" || exit 0
                    git push origin %BRANCH%

                '''
            }
        }
    }
}
