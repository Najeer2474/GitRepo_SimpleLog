pipeline {
  agent any
  environment {
      MAJOR = '1'
      MINOR = '0'
  }
  stages {
    stage ('PostBuild') {
      steps {
        UiPathDeploy (
          packagePath: "Project.json",
          orchestratorAddress: "https://cloud.uipath.com/wiprospydtqs/Najeer/orchestrator_/",
          orchestratorTenant: "Najeer",
          folderName: "All_Projects",
          credentials: [$class: 'UserPassAuthenticationEntry', credentialsId: “credentialsId”],
          traceLoggingLevel: 'None'
        )
      }
    }
  }
}
