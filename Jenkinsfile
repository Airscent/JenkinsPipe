pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    // stage('Install Arduino-CLI') {
    //     steps {
    //         // Arduino-CLI herunterladen und installieren
    //         sh '''
    //             wget https://github.com/arduino/arduino-cli/releases/download/v1.2.0-rc.1/arduino-cli_1.2.0-rc.1_Linux_ARM64.tar.gz
    //             tar -xzf arduino-cli_1.2.0-rc.1_Linux_ARM64.tar.gz 
    //             sudo mv arduino-cli /usr/local/bin/
    //             sudo arduino-cli config init
    //             sudo arduino-cli core install esp32:esp32
    //             arduino-cli board listall
    //         '''
    //     }
    // }
    stage('check arduino esp') {
      steps {
        sh 'arduino-cli board listall'
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
    
  }
}