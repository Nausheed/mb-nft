properties([
  parameters([
    choice(
      name: 'SNode',
      choices: "100.108.42.104\n100.108.42.236",
      description: 'Select a Stage Node to Deploy'
      )
  ])
])

pipeline{
  agent any
   parameters {
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
