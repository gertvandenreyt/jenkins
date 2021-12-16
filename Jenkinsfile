node {
    checkout scm

    docker.withRegistry('https://hub.docker.com/repository/docker/gertvandenreyt/jenkins', 'dockerhubsecret') {


        def customImage = docker.build("gertvandenreyt/jenkins:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
