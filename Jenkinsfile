pipeline {
  agent any
  stages {
    stage('Read YAML') {
      steps {
        script {
          // Read the yaml file from the workspace
          def yaml = readYaml file: 'manifest.yml'
          // Print some values from the yaml object
          echo "Name: ${yaml.name}"
          echo "Version: ${yaml.version}"
          echo "Description: ${yaml.description}"
          // Check if the yaml object has a key called 'items'
          if (yaml.plugin_name) {
            // Loop through the items array and print each element
            for (item in yaml.plugin-name) {
              echo "Item: ${item}"
            }
          }
        }
      }
    }
    // Other stages ...
  }
}
Copy