pipeline {
agent any
  environment { 
        def configVal = readYaml file: "test.yaml"
    }
  stages {
    stage("hello") {
                steps {
                    sh 'echo "sai"'
                  script {

                    def configVal = readYaml file: "test.yaml"
                    echo "configVal: " + configVal
                    def name = configVal['applications']['name'][0]
                    echo "name: " + name
                    
                  }
            }


    }


  }

}
