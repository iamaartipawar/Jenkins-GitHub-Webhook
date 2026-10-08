pipeline {
agent any

```
stages {

    stage('Checkout') {
        steps {
            echo 'Checking out source code from GitHub...'
        }
    }

    stage('Build') {
        steps {
            echo 'Building static website...'
        }
    }

    stage('Test') {
        steps {
            echo 'Testing website files...'

            sh '''
                test -f index.html
                test -f README.md
                echo "Required files are present."
            '''
        }
    }

    stage('Deploy') {
        steps {
            echo 'Deploying static website...'
            echo 'Deployment completed successfully.'
        }
    }
}

post {
    success {
        echo 'CI/CD Pipeline completed successfully!'
    }

    failure {
        echo 'Pipeline failed. Please check the console output.'
    }
}
```

}
