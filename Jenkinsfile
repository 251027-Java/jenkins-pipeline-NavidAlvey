groovy
pipeline {
    agent any
    
    tools {
        jdk 'JDK21'  // Must match the name from Task 3
    }
    
    stages {
        stage('Hello') {
            steps {
                echo 'Pipeline started!'
                echo "Building on: ${env.NODE_NAME}"
            }
        }
        
        stage('Checkout') {
            steps {
                // TODO: The checkout happens automatically when using 
                // "Pipeline script from SCM", but add an echo for visibility
                echo 'Code checked out from Git'
            }
        }
        
        stage('Build') {
            steps {
                // TODO: Make mvnw executable and run compile
                // Hint: Use sh 'chmod +x mvnw' and sh './mvnw clean compile'
            }
        }
        
        stage('Test') {
            steps {
                // TODO: Run the Maven tests
                // Hint: sh './mvnw test'
            }
        }
        
        stage('Package') {
            steps {
                // TODO: Create the JAR file, skipping tests (already ran)
                // Hint: sh './mvnw package -DskipTests'
            }
        }
    }
    
    post {
        success {
            echo '✅ Pipeline completed successfully!'
        }
        failure {
            echo '❌ Pipeline failed!'
        }
    }
}