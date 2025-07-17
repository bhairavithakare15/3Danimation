CODE_CHANGE = getGitChanges()
pipline {
  agent any 
  stages{
    stage('built'){
      when {
        expression {
          BRANCH_NAME == 'master' && CODE_CHANGES ==true
        }
      }
