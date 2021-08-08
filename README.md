# Github Actions - Java Gradle Dockerhub

#### Run on docker container
```bash
docker run -it --name gContainer --rm -u gradle -v "$PWD":/home/gradle/project -w /home/gradle/project gradle /bin/bash
```

⚠️ don't forget `-it` flag for running bash

Create a Gradle application
> gradle init
