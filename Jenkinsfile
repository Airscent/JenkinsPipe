pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage('Install Arduino-CLI') {
        steps {
            // Arduino-CLI herunterladen und installieren
            sh '''
                wget https://github.com/arduino/arduino-cli/releases/download/v1.2.0-rc.1/arduino-cli_1.2.0-rc.1_Linux_ARM64.tar.gz
                tar -xzf arduino-cli_1.2.0-rc.1_Linux_ARM64.tar.gz 
                mv arduino-cli /usr/local/bin/
                arduino-cli config init
                arduino-cli core install esp32:esp32
                arduino-cli board listall
            '''
        }
    }
    stage('hello python') {
      steps {
        sh 'python3 hello.py'
      }
    }
    stage('build all version') {
        steps {
            script {
                def brands = ['Airscent', 'Begeuren','ToTest']
                def moddels = ['Quad', 'Octo', 'Venturi','Aromare']
                brands.each { brand ->
                    moddels.each { model ->
                    echo "Build brand: ${brand} ${model}"

                    //echo "change config file:"
                    //sh 'cat config.c'

                    }
                }
            }
        }
    }
    stage('check arduino') {
      steps {
        sh 'arduino-cli board listall'
      }
    }
  }
}