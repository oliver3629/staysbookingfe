# Stays Booking Frontend

React frontend for Staybooking. Guests can search stays and manage reservations; hosts can upload and manage listings and view bookings.

## Technology

- React and Create React App
- Ant Design for the user interface
- Fetch API for backend requests

## Project structure

| File | Purpose |
| --- | --- |
| `src/App.js` | Login state and host/guest views |
| `src/components/LoginPage.js` | Registration and login |
| `src/components/HostHomePage.js` | Host listings and bookings |
| `src/components/GuestHomePage.js` | Stay search and reservations |
| `src/components/UploadStay.js` | New listing form |
| `src/utils.js` | Backend API requests |

## Run locally

Install Node.js and npm. From the project directory, run:

```sh
npm install
npm start
```

Open `http://localhost:3000`. Before starting, set `const domain` at the top of `src/utils.js` to `http://localhost:8080` for a local backend, or to your deployed backend URL if you use the hosted API. Do not leave it empty.

## Deploy to AWS Amplify

1. Set `const domain` in `src/utils.js` to your deployed backend URL, then build the frontend:

   ```sh
   npm run build
   ```

2. Create a ZIP file containing the **contents** of `build/`, not the `build` folder itself. `index.html` should be at the ZIP root.
3. Open the [AWS Amplify console](https://us-east-2.console.aws.amazon.com/amplify/apps?region=us-east-2) and choose **Create new app** → **Deploy without Git** → **Next**.
4. Enter an app name and branch name, choose **Drag and drop**, select the ZIP file, then choose **Save and deploy**.

See the [AWS manual deployment guide](https://docs.aws.amazon.com/amplify/latest/userguide/manual-deploys.html) for the console steps.
