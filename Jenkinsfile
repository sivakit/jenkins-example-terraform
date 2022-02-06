pipeline {
    agent any
    options {
        timeout(time: 30, unit: 'MINUTES') 
    }
       stages {
           stage("reading properties from properties file") {
               steps {
                    script {
                    def props = readProperties file: 'version.properties' 
                    env.Version = props.version
                   }
                echo "The username  is $Version"
               }
           }
        stage('Example') {
            steps {
                echo 'Hello World $Version'
            }
        }
    }
}
