node {
    checkout scm

    docker.withRegistry('https://github.com/gertvandenreyt/jenkins', 'dockerhub') {


        def customImage = docker.build("gertvandenreyt/jenkins:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
