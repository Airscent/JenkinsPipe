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
                def brands = ['Airscent', 'Begeuren']
                def moddels = ['Quad', 'Octo', 'Venturi','Aromare']
                brands.each { brand ->
                    moddels.each { model ->
                    echo "Build brand: ${brand} ${model}"
                    echo "change config file:"

                    sh 'cat /config.c'


                    }
                }
            }
        }
    }
  }
}