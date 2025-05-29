# {{ project-name }}

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 19.2.12.

## Development server

To start a local development server, run:

```bash
ng serve
```

Once the server is running, open your browser and navigate to `http://localhost:4200/`. The application will automatically reload whenever you modify any of the source files.

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Karma](https://karma-runner.github.io) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.

## Promoting Images

Upon each commit to main, the Docker image is built and deployed to the dev Kubernetes cluster automatically. However, the process to promote an image to stg or prd requires a couple of manual button presses, allowing you to control when to deploy images to other environments.

1. Launch a run of [**Cut Release Tag**](.github/workflows/cut-tag.yaml) — this will bump the version number of the application, publish a new docker image to Artifactory with the necessary tags, and create a new Github release from that tag. Make sure to select the appropriate level to bump, conforming with [semantic versioning](https://semver.org/).
2. Launch a run of [**Promote Tag**](.github/workflows/promote.yaml) — this will take an existing docker image and promote it to the specified environment. Make sure to enter the Github tag you wish to promote (created by **Cut Release Tag** from step one) and the environment to which you wish to promote the image.
