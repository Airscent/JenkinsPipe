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
                    def file = new File('config1.c')
                    def lines = file.readLines()
                    //if (lines.size() >= 1) {
                    //    lines[2] = "AsBrand = '${brand}';"
                    //    lines[3] = "AsModel = '${model}';"
                    //}
                    //file.text = lines.join('\n')
                    sh 'cat config1.c'

                    }
                }
            }
        }
    }
  }
}