[![Java CI with Gradle](https://github.com/AmirNaghibi/github-actions-gradle-docker-cs/actions/workflows/ci.yml/badge.svg)](https://github.com/AmirNaghibi/github-actions-gradle-docker-cs/actions/workflows/ci.yml)

# Github Actions - Java Gradle Dockerhub
- [Tutorial Video](https://www.youtube.com/watch?v=R8_veQiYBjI&ab_channel=TechWorldwithNana)
- [Tutorial Repo](https://github.com/nanuchi/my-project)
#### Run docker container to setup gradle repo
```bash
docker run -it --name gContainer --rm -u gradle -v "$PWD":/home/gradle/project -w /home/gradle/project gradle /bin/bash
```

⚠️ don't forget `-it` flag for running bash

Create a Gradle application
> gradle init

##### build the project

    ./gradlew build

##### build Docker image called java-app. Execute from root

    docker build -t java-app .
    
##### push image to repo 

    docker tag java-app demo-app:java-1.0