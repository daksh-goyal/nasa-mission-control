# NASA Mission Control

NASA Mission Control is a mock space mission control dashboard. It lets users schedule missions to other most habitable exoplanets from a list of planets explored by the [Kepler](https://www.nasa.gov/mission_pages/kepler/main/index.html) spacecraft. This project uses [React](https://reactjs.org/) in frontend and [NodeJS](https://nodejs.org/en/) in backend. The database used is [MongoDB Atlas](https://www.mongodb.com/cloud/atlas). This project also uses a [SpaceX API](https://github.com/r-spacex/SpaceX-API) to provide information about the past and upcoming SpaceX launches. The project can be tried out [here](https://nasa-mission-control.herokuapp.com/).

## Installation and Set Up

1. Clone this repo

   ```sh
   git clone https://github.com/daksh-goyal/nasa-mission-control.git
   cd nasa-mission-control
   ```

2. Get the latest version of node for your OS from the official [NodeJS](https://nodejs.org/en/) website.

3. Install all the dependencies

   ```sh
   npm install
   ```
   
4. Start the development server

   ```sh
   npm run watch
   ```
## Building and Deploying

1. Generate a production build 

   ```sh
   npm run build
   ```
 
2. Deploying on a VM

    The code can be deployed to a virtual machine. After setting up the environment, you can run the build command to start a production build. 
    Note: You can also generate a dockerfile instead and use docker to run your production build.

### Building a Docker image

1. Install Docker using their dedicated install [guide](https://docs.docker.com/engine/install/) for your specific OS.

2. Inside the cloned directory run the following command

    ```sh
   docker build . -t {yourDockerUsername}/{imageName}
   ```
   
   Alternatively, if you wish to use Github Actions to build and push your Docker image to DockerHub, you need to set the following GitHub secrets

    ```
    DOCKERHUB_TOKEN
    DOCKERHUB_USERNAME
    ```
    
    Note: The GitHub action in this repo is configured to run everytime you push a commit to the main branch. 
   
## Packages Used

1. [Mongoose](https://mongoosejs.com/) for MongoDB in Node.
2. [Morgan](https://www.npmjs.com/package/morgan) for logging.
3. [PM2](https://pm2.keymetrics.io/) for load balancing and zero downtime restart.
4. [Arwes](https://arwes.dev/) for giving the webpage that sci-fi feel.
