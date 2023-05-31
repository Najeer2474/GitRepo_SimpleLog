pipeline {
  agent any
  environment {
      MAJOR = '1'
      MINOR = '0'
      Path  = 'C:\ProgramData\UiPath\Packages\SimpleLog.1.0.1.nupkg'
  }
  stages {
    stage ('PostBuild') {
      steps {
        UiPathDeploy (
          packagePath: "${Path}" ,
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
