# **AI Image Generation App**

### _A MERN Stack Project_

<br>

# Table of Contents

- [Project Description](#description)
- [Application Improvements (Optional)](#improvements)
- [How To Setup](#setup)
- [Credits](#credits)

<br>

## **Description**

Welcome fellow developer, thank you for your interest in this project. I created projects like this to mainly put into practice and deep dive into the React library and at the same time learn some backend technologies.

This is SALL-E (DALL-E clone), an AI image generation app where users can showcase their resulting image based on their entered prompt. [**MongoDB Atlas**](https://firebase.google.com/) serves as the Database for user's name, prompt used, and the URL of the image generated which was saved and hosted in [**Cloudinary**](https://cloudinary.com/). [**Node.js**](https://nodejs.org/en/) with [**Express**](https://expressjs.com/) was used for the backend while the [**React library**](https://reactjs.org/) for the frontend. Styling was done using [**TailwindCSS**](https://tailwindcss.com/).

<br>

## **Improvements**

- It may add some friction, but a user authentication will serve as added security.

<br>

## **Setup**

<br>

### **SERVER**

1. You can either [clone](https://github.com/its-me-lenny/ai-image-generator-app.git) the repository or [download](https://github.com/its-me-lenny/ai-image-generator-app.git) and extract it in your local machine.

2. Follow steps 1-5 in [here](https://www.mongodb.com/docs/atlas/getting-started/#std-label-atlas-getting-started) to create your free cluster in [MongoDB Atlas](https://www.mongodb.com/atlas/database) until you get access to your connection string that looks like this `"mongodb+srv..."`.

   _Note: Your username is pre filled in the connection string but you have to enter the user password manually._

3. Create an _.env_ file in the root directory of the **server** folder and put the connecton string in an environment variable exactly like this:

   > `MONGODB_URL= {Your connection string}`

   This will help prevent others to have access to your _secrets_ if you are planning to share the codebase to others.

4. Generate a secret key in [OpenAI](https://openai.com/api/).

   1. Make sure that you have an account and you are logged in.
   2. Click on your username at the top-right corner.
   3. Click **_View API keys_**
   4. Click **_Create new secret key_**
   5. Add it in the _.env_ file too like this:

   <br>

   > `OPEN_AI_KEY= {Your secret key}`

5. Create an account in [Cloudinary](https://cloudinary.com/users/register_free#gsc.tab=0).

   1. Go to the Dashboard.
   2. Save the ff:
      - Cloud Name
      - API Key
      - API Secret
   3. Add them as environment variables as so:

   <br>

   > `CLOUDINARY_CLOUD_NAME = {Cloud Name}` <br> `CLOUDINARY_API_KEY = {API Key}` <br> `CLOUDINARY_API_SECRET = {API Secret}`

6. Run the following command on the root directory of the codebase:

   > `npm install`

7. After succesfull installation of dependencies, you can now run the command:

   > `npm start`

   to start serving the app on your local machine.

<br>

### **CLIENT**

1. Create and add an environment variable in your _.env_ file in the root directory of the client folder:

   > `VITE_SERVER_URL = http://localhost:8080/api/v1/dalle`

   _Note: If you have deployed the server, change this URL to the production URL of your server._

2. Run the following command on the root directory of the codebase:

   > `npm install`

3. After succesfull installation of dependencies, you can now run the command:

   > `npm run dev`

   to start serving the app on your local machine.

4. Play around with the app and enjoy!

5. If you want to deploy the app, just initiate the command:

   > `npm run build`

   After that, you can use the _dist_ folder in the root directory for your production deployment.

<br>

## **Credits**

- For download image functionality, [file-saver](https://github.com/eligrey/FileSaver.js).
- For routing, [react-router-dom](https://reactrouter.com/en/main/start/tutorial).
- For schema, [Mongoose](https://mongoosejs.com/).
- For reading .env file in Nodejs, [dotenv](https://github.com/motdotla/dotenv).
- For monitoring scripts during development, [nodemon](https://nodemon.io/)
- [Tutorial and inspiration](https://www.youtube.com/watch?v=EyIvuigqDoA&t=1s) from [JavascriptMastery](https://www.youtube.com/@javascriptmastery) ([adrianhajdin](https://github.com/adrianhajdin) on GitHub).
- [Vite](https://vitejs.dev/) for bootstrapping the project.
