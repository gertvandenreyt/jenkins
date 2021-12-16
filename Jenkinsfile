node {
    checkout scm
    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
        def customImage = docker.build("gertvandenreyt/postgresql13:${env.BUILD_ID}")
        /* Push the container to the custom Registry */
        customImage.push()
    }
}
