node {
    checkout scm

    docker.withRegistry('https://github.com/gertvandenreyt/jenkins', '9347288c-9c72-4f59-9f85-cc667bafc5ec') {


        def customImage = docker.build("gertvandenreyt/jenkins:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
