# ci-cd-final-project

Project name: **ci-cd-final-project**

A RESTful counter microservice (Flask) with a full CI/CD setup:

- **CI:** GitHub Actions workflow (`.github/workflows/workflow.yml`) that lints with flake8 and runs unit tests with nose on every push and pull request to `main`.
- **CD:** OpenShift Pipelines (Tekton) with custom tasks (`.tekton/tasks.yml`: `cleanup`, `nose`) and a pipeline (`.tekton/pipeline.yml`) that cleans the workspace, clones the repo, lints, tests, builds an image with buildah, and deploys it to the lab OpenShift cluster.
