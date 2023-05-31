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
          packagePath: 'C:\ProgramData\UiPath\Packages\SimpleLog.1.0.1.nupkg',
          orchestratorAddress: "https://cloud.uipath.com/",
          orchestratorTenant: "Najeer",
          folderName: "Projects",
          environments: "",
          //credentials: [$class: 'UserPassAuthenticationEntry', credentialsId: “credentialsId”]
          credentials: Token(accountName: "wiprospydtqs", credentialsId: 'APIUserKey'),
          traceLoggingLevel: 'None'
        )
      }
    }
  }
}
