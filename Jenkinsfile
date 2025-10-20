pipeline {
    agent any

    stages {
        stage('Preparar entorno') {
            steps {
                echo "Creando entorno virtual..."
                bat '"C:\Users\karol\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Python 3.13\Python 3.13 (64-bit).lnk" -m venv venv'
                bat 'venv\\Scripts\\activate && pip install -r requirements.txt'
            }
        }

        stage('Ejecutar script') {
            steps {
                echo "Ejecutando script principal..."
                bat 'C:\Users\karol\OneDrive\Escritorio\PYTHON\CLASE\Pruebajenkins.py'
            }
        }
    }

    post {
        success { echo "✅ Pipeline completado con éxito" }
        failure { echo "❌ Error en alguna etapa del pipeline" }
    }
}
