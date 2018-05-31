pipeline {
  agent none
  stages {
    stage('BuildStage') {
      steps {
        build 'SampleBuildJob'
      }
    }
    stage('DeployStage') {
      parallel {
        stage('DeployStage') {
          steps {
            build 'SampleDeployJob'
          }
        }
        stage('DeployStage2') {
          steps {
            build 'SampleDeployJob2'
          }
        }
        stage('DeployStage3') {
          steps {
            build 'SampleDeployJob3'
          }
        }
      }
    }
    stage('Teststage') {
      steps {
        build 'SampleTestJob'
      }
    }
  }
}