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

### Learning Outcomes 👨🏼‍🎓
- Understand basics of GitHub Actions
    - definition of [Event](https://docs.github.com/en/actions/reference/events-that-trigger-workflows) vs [Action](https://docs.github.com/en/actions/learn-github-actions/introduction-to-github-actions)
    - use repository secrets `secrets.DOCKER_USERNAME`
    - adding CI Tag from Actions tab
    - use pre-built actions
- Run current directory inside a docker container
- Generate Gradle App with `gradle init`
- Each commit is a high-quality independent piece of work `git reset --soft HEAD~1`
    - or just use vscode > source control > COMMITS tab to undo a commit and then force push
