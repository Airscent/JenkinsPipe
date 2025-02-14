pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage('hello') {
      steps {
        sh 'python3 hello.py'
      }
    }
    stage('Iteration über ein Array') {
        steps {
            script {
                def brands = ['Apfel', 'Banane', 'Orange']
                def moddels = ['Quad', 'Octo', 'Venturi','Aromare']
                brands.each { brand ->
                    moddels.each { model ->
                    echo "Build brand: ${brand} ${model}"

                    
                    }
                }
            }
        }
    }
  }
}