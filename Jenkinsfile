node('nodejs') {
  stage 'build'
  openshiftBuild(buildConfig: 'nodejs-ex', showBuildLogs: 'true')
  stage('test') {
      steps {
          echo 'Testing..'
          npm test
      }
  }
  stage 'deploy'
  openshiftDeploy(deploymentConfig: 'nodejs-ex')
}
