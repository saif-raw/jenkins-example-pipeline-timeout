pipeline {
  agent none
  options {
    timeout(time: 301, unit: 'SECONDS') 
  }
  stages {
    stage('input') {
      agent any
      input {
        message "What is your first name?"
        ok "Submit"
        parameters {
          string(defaultValue: 'Dave', name: 'FIRST_NAME', trim: true) 
        }
      }
      options {
        timeout(time: 60, unit: 'SECONDS') 
      }
      steps {
        echo "Good Morning, $FIRST_NAME"
        sh '''
          hostname
          cat /etc/redhat-release
        '''
      }
    }
  }
}
