#!groovy

node {
   stage 'Checkout'
        checkout scm

   stage 'Setup'
        sh '/opt/node/bin/npm install'

   stage 'Mocha test'
        sh './node_modules/moch/bin/mocha'

   stage 'Cleanup'
        echo 'prune and cleanup'
        sh '/opt/node/bin/npm prune'
        sh 'rm node_modules -rf'
}
