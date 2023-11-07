node {
    checkout scm

    // BUILD
    stage("Build"){
        docker.image('shippingdocker/php-composer:7.4').inside('-u root') {
            sh 'rm composer.lock'
            sh 'composer install'
        }
    }

    // TEST
    stage("Test"){
        docker.image('ubuntu').inside('-u root') {
            sh 'echo "Ini adalah test"'
        }
    }

    // DEPLOY
    stage("Deploy"){
        docker.image('ubuntu').inside('-u root') {
            sh 'echo "Ini adalah deploy"'
        }
    }
}