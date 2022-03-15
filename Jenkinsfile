import groovy.json.JsonSlurperClassic

def jsonParse(def json) {
    new groovy.json.JsonSlurperClassic().parseText(json)
}

pipeline {
    agent any
    stages {
        stage("Paso 0: Jmeter"){
            steps {
                script {
                    sh "mvn verify -Pperformance"
                }
            }
        }
    }
}
