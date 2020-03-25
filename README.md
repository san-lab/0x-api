## Introduction

This is a fork of 0xAPI used for Blablapay use case.

## Deploying

To get a local development version of `0x-api` running:

1. Clone the repo.

2. Copy .env_example into .env

3. Install the dependencies:

    ```sh
    yarn
    ```

4. Build the project:

    ```sh
    yarn build
    ```

5) Run `docker-compose up` to run the other dependencies required for the API. This uses the local `docker-compose.yml` file.  If you do it after a prior run, you will have to `rm -rf 0x_mesh postgres` to delete the volumes containing stale data.

6) Start the API

    ```sh
    yarn dev
    ```

## In case of failure

In the release there is three artifacts:

- node_modules and two docker images.

If the API do not work properly, this might be because of some dependency broken out of our control.

In this case, instead of the step 3, extract node_modules.tgz in the root folder and, before step 5, load the ganache and mesh images using the command:

```
docker load --input <file_name>
```


## Legal Disclaimer

The laws and regulations applicable to the use and exchange of digital assets and blockchain-native tokens, including through any software developed using the licensed work created by ZeroEx Intl. as described here (the “Work”), vary by jurisdiction. As set forth in the Apache License, Version 2.0 applicable to the Work, developers are “solely responsible for determining the appropriateness of using or redistributing the Work,” which includes responsibility for ensuring compliance with any such applicable laws and regulations.
See the Apache License, Version 2.0 for the specific language governing all applicable permissions and limitations: http://www.apache.org/licenses/LICENSE-2.0
