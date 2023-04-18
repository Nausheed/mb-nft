pipeline{
  agent any
   parameters {
               choice(name: 'ACTION', choices: ['deploy', 'rollback'], description: 'Choose action: deploy or rollback')
               choice(name: 'ACTION', choices: ['100', '101'], description: 'Choose action: 100 or 101')
    }
  stages{
    stage("clone"){
      steps{
      echo "cloning"
      }
    }
  }
}
