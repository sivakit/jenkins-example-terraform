properties = null

def loadProperties() {
    node {
        checkout scm
        properties = readProperties file: 'version.properties'
    }
}
pipeline {
    agent any
    options {
        timeout(time: 30, unit: 'MINUTES') 
    }
       stages {
           stage("reading properties from properties file") {
               steps {
                    script {
                        loadProperties()
                   }
                echo "The username  is ${properties.version}"
               }
           }
        stage('Example') {
            steps {
                echo "${properties.version}"
            }
        }
    }
}
