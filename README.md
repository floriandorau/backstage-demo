# [backstage-demo](https://backstage.io)

Backstage demo application used as a playground to test Backstage capablilites.

## Pre-Installed plugins

This Backstage demo contains pre-installed plugins

- [Github Insights](https://github.com/RoadieHQ/roadie-backstage-plugins/tree/main/plugins/frontend/backstage-plugin-github-insights)
- [Github Security Insights](https://github.com/RoadieHQ/roadie-backstage-plugins/tree/main/plugins/frontend/backstage-plugin-security-insights)
- [Github Pull Requests Insights](https://github.com/RoadieHQ/roadie-backstage-plugins/tree/main/plugins/frontend/backstage-plugin-github-pull-requests)
- [ArgoCD](https://github.com/RoadieHQ/roadie-backstage-plugins/tree/main/plugins/frontend/backstage-plugin-argo-cd)
- [Bulletin Board](https://github.com/v-ngu/backstage-plugin-bulletin-board/tree/main/plugins/bulletin-board-backend)

## Prerequisites

Before you can start Backstage demo application you need to create a local configuration file. Create a file named `app-config.local.yaml` with the following configuration.

```yaml
integrations:
  github:
    - host: github.com
      token: <redacted>

auth:  
  environment: development
  providers: 
    github:
      development:
        clientId: <redfacted>
        clientSecret: <redacted>
```

Make sure you have working Github personal access token and Github OAuth app `clientId` and `clientSecret`. 

## Start

To start the app, run:

```shell
# Install dependencies
yarn install
```

```shell
# Start application
yarn dev
```

After starting Backstage application you can visit `Http://localhost:3000`.

## Kubernetes & ArgoCD integration

For Kubernetes & ArgoCD integration running please refer to proper infrastructure setup in [backstage-app-deployments](https://github.com/floriandorau/backstage-app-deployments).
