pipeline {
  agent any
  options { ansiColor('xterm'); timestamps() }

  stages {
      stage('Clone')
      steps {
    git branch: 'main' ,  url: "https://github.com/km-programmer/KUV-Test.git"
  }
  }
    stage('Hello')
    {
      steps {
        echo 'Starting build…'
      }
    }

    stage('Run some commands') {
      steps {
        sh '''
          echo "User: $(whoami)"
          echo "Host: $(hostname)"
          echo "Pwd : $(pwd)"
          echo "Date: $(date -Is)"
          echo "Workspace contents:"
          ls -lah
        '''
      }
    }

    stage('Capture and print a command output') {
      steps {
        script {
          def kernel = sh(script: 'uname -r', returnStdout: true).trim()
          echo "Kernel version: ${kernel}"
        }
      }
    }

    stage('Show environment variables') {
      steps {
        sh 'printenv | sort'
      }
    }
  }
}
