#!groovy
pipeline {
   agent any
    options{
       timestamps()
       ansiColor('xterm')
   }
   stages {
      stage('List All Images') {
         steps {
             script{
                    sh ''' docker image ls
                    '''
                    myscript.info("Successfully Executed")
                   # def ret = sh(script: 'dooocker image ls', returnStatus: true)
                   # myscript.warning(ret)
             }
         }
      }
      stage('Git Commit Id') {
         steps {
              script{
		    echo '$(git rev-parse HEAD)
		    #def gitId=sh(script:'git rev-parse HEAD', returnStdout: true)
                    #myscript.gitCommitId($(git rev-parse HEAD))
             }
         }
      }
   }
}
