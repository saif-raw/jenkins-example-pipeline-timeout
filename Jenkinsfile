pipeline {
  agent none
  stages {
    stage('input') {
      agent any
      input {
        message "Organisation"
        ok "Submit"
        parameters {
          string(defaultValue: 'Contentstack', name: 'COMPANY_NAME', trim: true) 
        }
      }
      options {
        timeout(time: 120, unit: 'SECONDS') 
      }
      steps {
        echo "Hello from $COMPANY_NAME"
        sh '''
          hostname
          cat /etc/redhat-release
        '''
      }
    }
  }
}
