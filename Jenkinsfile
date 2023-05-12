pipeline {
  agent any
  stages {
    stage('Read YAML') {
      steps {
        script {
          // Read the yaml file from the workspace
          def yaml = readYaml file: 'manifest.yml'
          // Check if the yaml object has a key called 'items'
          if (yaml.plugin_name) {
            // Loop through the items array and print each element
            for (item in yaml.plugin_name) {
              echo "Item: ${item}"
            }
          }
        }
      }
    }
    // Other stages ...
  }
}