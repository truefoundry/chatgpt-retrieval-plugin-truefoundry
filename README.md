# chatgpt-retrieval-plugin-truefoundry

## A guide to deploying ChatGPT Retrieval Plugin on TrueFoundry

To deploy the Docker container from this repository to TrueFoundry, follow these steps:

### 1. Create a free account with [TrueFoundry](https://app.truefoundry.com/) and create a new workspace with a unique name.
### 2. Go to the [secrets console](https://app.truefoundry.com/secrets). Create a new secret group and create secrets for your chosen vector DB. You can find the list of environment variables needed for each vector DB [here](https://github.com/openai/chatgpt-retrieval-plugin#choosing-a-vector-database).
    ![create secret group](./create-secret-group.png)
### 3. Go to the [deployment console](https://app.truefoundry.com/deployments). Create a new service in your workspace.
    ![create service](./create-service.png)
### 4. In the form, set the source to the Github repo URL (https://github.com/openai/chatgpt-retrieval-plugin) and the build to DockerFile build.
   ![source & build setting](./source-build.png)
### 5. In the form, set the port to 8080
   ![port setting](./port-setting.png)
### 6. Add the environment variables and set them to the secrets you just created.
   ![env setting](./setting-envs.png)
### 7. Deploy and your plugin webapp and endpoint should show up in the [deployments tab](https://app.truefoundry.com/deployments).
![deployed service](./deployed-svc.png)

