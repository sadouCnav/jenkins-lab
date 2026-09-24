pipeline {
    agent any
    stages {
        stage('Compilation & Tests') {
            parallel {
                stage('Build') {
                    steps {
                        echo "Compilation en cours..."
                         'sleep 3' // Simulation du build
                         bat 'timeout /t 3 /nobreak > nul'
                    }
                }
                stage('Tests Unitaires') {
                    steps {
                        echo "Exécution des tests unitaires..."
                        bat 'sleep 2' // Simulation des tests unitaires
                    }
                }
                stage('Analyse Qualité') {
                    steps {
                        echo "Analyse statique du code avec SonarQube..."
                        bat 'sleep 4' // Simulation de l’analyse
                    }
                }
            }
        }
    }
}