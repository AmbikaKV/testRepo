pipeline {
  agent any
  stages {
    stage('downloadSDK') {
      steps {
        sh 'curl -O http://nexus.wdf.sap.corp:8081/nexus/content/repositories/deploy.milestones/com/sap/it/spc/chs/stack.chs/1.32.0/stack.chs-1.32.0-assembly.zip'
      }
    }
    stage('readConfigFileForDCdetails') {
      steps {
        echo 'Yet to figure what to add here'
        readFile(file: '/DCDetails.xml', encoding: 'XML')
      }
    }
    stage('DC1 update') {
      parallel {
        stage('DC1 update') {
          steps {
            echo 'yet to update this section'
          }
        }
        stage('DC2 update') {
          steps {
            echo 'yet to update the script'
          }
        }
      }
    }
    stage('mail') {
      steps {
        emailext(subject: 'update done', body: 'you can monitor the app status for next couple of hours', to: 'ambika.kv@sap.com')
      }
    }
  }
}