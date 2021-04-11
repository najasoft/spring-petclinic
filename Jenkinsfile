pipeline {
  agent any
  stages {
    stage('Git') {
      parallel {
        stage('Git') {
          steps {
            build(job: 'test', propagate: true)
          }
        }

        stage('build') {
          steps {
            archiveArtifacts(allowEmptyArchive: true, caseSensitive: true, defaultExcludes: true, artifacts: 'target/*.jar')
          }
        }

      }
    }

  }
}