### Express backend to handle form submission
- Handles a react form in this [repo](https://github.com/BulegaHassan/personal-porfolio).
- Uses Nodemailer and oAuth2.
- Follow this [guide](https://dev.to/jlong4223/how-to-implement-email-functionality-with-node-js-react-js-nodemailer-and-oauth2-2h7m) for a step by step setup.
- Deployed on [render] (https://render.com/)
### Getting started
- Install packages and start server
```bash 
   npm install && npm start
```

### .env variables
```js
let transporter = nodemailer.createTransport({
 service: "gmail",
 auth: {
   type: "OAuth2",
   user: process.env.EMAIL,
   pass: process.env.WORD,
   clientId: process.env.OAUTH_CLIENTID,
   clientSecret: process.env.OAUTH_CLIENT_SECRET,
   refreshToken: process.env.OAUTH_REFRESH_TOKEN,
 },
});
```
- EMAIL is your email and WORD is your password
- clientId, clientSecret and refreshToken are got from [GCP](https://console.cloud.google.com/) . Follow this [guide](https://dev.to/jlong4223/how-to-implement-email-functionality-with-node-js-react-js-nodemailer-and-oauth2-2h7m) for clarity.
