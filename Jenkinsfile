pipeline{
  agent any
   parameters {
        string(name: 'SERVER_1', defaultValue: '', description: 'Server 1 URL')
        string(name: 'SERVER_2', defaultValue: '', description: 'Server 2 URL')
        choice(name: 'ACTION', choices: ['deploy', 'rollback'], description: 'Choose action: deploy or rollback')
    }
  stages{
    stage("clone"){
      steps{
      echo "cloning"
      }
    }
  }
}
