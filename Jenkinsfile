node {
  stage('Wait for user to input text?') {
    steps {
        script {
             def userInput = input(id: 'userInput', message: 'Merge to?',
             parameters: [[$class: 'ChoiceParameterDefinition', defaultValue: 'strDef', 
                description:'describing choices', name:'nameChoice', choices: "QA\nUAT\nProduction\nDevelop\nMaster"]
             ])

            println(userInput); //Use this value to branch to different logic if needed
        }
    }
  }
  stage ('clone') {
    git 'https://github.com/slowslipper/build-playground.git'
  }
  stage ('install') {
    sh 'yarn install'
  }
  stage ('build') {
    sh 'yarn build'
  }
}