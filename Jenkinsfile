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
            def output = ''
            for (item in yaml.plugin_name) {
              output += item + ','
            }
            // Remove the last comma from the output string
            output = output[0..-2]
            // Print the output string
            echo "Output: ${output}"
          }
        }
      }
    }
    // Other stages ...
  }
}