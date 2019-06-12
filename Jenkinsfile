node {

    checkout scm

    env.DOCKER_API_VERSION="1.23"
    
    sh "git rev-parse --short HEAD > commit-id"

    tag = readFile('commit-id').replace("\n", "").replace("\r", "")
    appName = "iris_classification"
    registryHost = "ksr1729/"
    imageName = "${registryHost}${appName}:${tag}"
    env.BUILDIMG=imageName

    stage "Build"
    
       sh "s2i build . seldonio/seldon-core-s2i-python3 ${imageName}" 

    stage "Push"

        sh "docker push ${imageName}"

}
