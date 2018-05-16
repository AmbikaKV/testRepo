pipeline {
  agent any
  stages {
    stage('downloadSDK') {
      steps {
        sh 'curl -O http://nexus.wdf.sap.corp:8081/nexus/content/repositories/deploy.milestones/com/sap/it/spc/chs/stack.chs/1.32.0/stack.chs-1.32.0-assembly.zip'
      }
    }
  }
}