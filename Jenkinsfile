node {
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