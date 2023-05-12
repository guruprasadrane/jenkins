pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
       stage('Read YAML file') {
        steps {
            script{ datas = readYaml (file: 'manifest.yml') }
            echo datas.ear_file.deploy.toString()

        }
    }
    }

}
