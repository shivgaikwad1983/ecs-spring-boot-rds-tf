node {
  stage 'Checkout'
 
  stage 'Docker build'
  docker.build('demo')
 
  stage 'Docker push'
  docker.withRegistry('035898547283.dkr.ecr.eu-central-1.amazonaws.com/provectus-app-test', 'ecr:us-east-1:demo-ecr-credentials') {
    docker.image('demo').push('latest')
  }
}
