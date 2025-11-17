pipeline {
    agent any
    environment { // variables defined here can be used by any stage
        NEW_VERSION = '1.3.0'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
                // To output the value of variable in string use " "
                echo "Building version ${env.NEW_VERSION}"
            }
        }
// ... other stages ...
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Here you can define commands for your build
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                // Here you can define commands for your tests
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // Here you can define commands for your deployment
            }
        }
    }
}

// ... end of stages block
    }
}
post {
    always { // This action will happen regardless of the result of build
        echo 'Post build condition running'
    }
    failure { // This action will happen only if the build has failed
        echo 'Post Action if Build failed'
    }
}
// ... end of pipeline block
