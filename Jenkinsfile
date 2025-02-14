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
                def fruits = ['Apfel', 'Banane', 'Orange']

                // Verwendung von each
                fruits.each { fruit ->
                    echo "Frucht: ${fruit}"
                }

                // Verwendung von eachWithIndex
                fruits.eachWithIndex { fruit, index ->
                    echo "Frucht Nr. ${index + 1}: ${fruit}"
                }
            }
        }
    }
  }
}