# Week 5-6 Exercise Evidence

Name: Alexander McMillan
GitHub repository URL: 

## Part A - Starting validation
- Local pytest result: Success
- Initial CI workflow run URL:https://github.com/mcmillanam/SDI4213IndProj/actions/runs/37400034624

## Part B - Week 5 build automation
- Pull request URL: https://github.com/mcmillanam/SDI4213IndProj/pull/2
- Successful workflow run URL: https://github.com/mcmillanam/SDI4213IndProj/actions/runs/37411298709
- Artifact name: sdi4213-app
- What files are inside the downloaded artifact? requirements.txt, README.md, and VERSION.

## Part C - Version and release
- Version: 0.1.0
- Git tag: v0.1.0
- GitHub Release URL: https://github.com/mcmillanam/SDI4213IndProj/releases/tag/v0.1.0
- Short release-note summary: This release packages the FastAPI inventory application for the Week 5 build automation exercise. The project includes automated pytest testing through Github Actions and an automated ZIP build artifact containing the application files, requirements.txt, README.md, and VERSION.

## Part D - Week 6 Docker
- Docker image name and tag: sdi4213-week56:0.1.0
- `docker images` evidence:![Milestone 6 - Versioned Docker image built successfully.](<Week56-06 Versioned Docker Image.png>)
- `docker ps` evidence:![Milestone 7 - Container is running and port 8000 is published.](<Week56-07 Running Container.png>)
- `/health` response:![Milestone 8 - Containerized application health check succeeds.](<Week56-08 Health Check.png>)
- `docker logs` evidence:![Milestone 9 - Container logs confirm the application started and handled requests.](<Week56-09 Container Logs.png>)

## Reflection
1. What is the difference between a workflow artifact and a Docker image?
    A workflow artifact is a file produced and stored by a CI workflow, such as the ZIP package created by GitHub Actions. It's useful for keeping and sharing a build output. A Docker image is a packaged version of the application that includes everything needed to create a running container.
2. Why did you tag the Git release and Docker image with a version?
    So that they are clearly identified as belonging to the same version of the application. This makes it easier to track changes.
3. What does `-p 8000:8000` do?
    This option maps port 8000 on my computer to port 8000 inside the Docker container.
4. What would you automate next if this project were moving toward deployment?
    It would probably be best to automate deployment after the tests and Docker image build succeed.

Additional Screenshots:
![Milestone 1 - Starter tests pass locally before modifications.](<Week56-01 Local Tests Screenshot-1.png>)
![Milestone 2 - Baseline GitHub Actions CI workflow passes.](<Week56-02 Verify Workflow Screenshot.png>)
![Milestone 3 - CI created and uploaded the build artifact.](<Week56-03 Build Artifact.png>)
![Milestone 4 - Downloaded artifact containes the required release files.](<Week56-04 Build Artifact Downloaded.png>)
![Milestone 5 - Versioned GitHub Release v0.1.0 published.](<Week56-05 Versioned GitHub Release.png>)
![Milestone 10 - Containerization changes passed CI and were merged through the pull request workflow.](<Week56-10 Final Pull Request and CI.png>)