# zoommeeting-sdk-angular-app


Zoom Meeting SDK Angular sample
Use of this sample app is subject to our Terms of Use.

This repo is an Angular app generated via the Angular CLI that uses the Zoom Meeting SDK to start and join Zoom meetings and webinars.

Zoom Meeting SDK Client View

Installation
To get started, clone the repo:

$ git clone https://github.com/zoom/meetingsdk-angular-sample.git

To setup and run the app you will need the Angular CLI.

Setup
Once cloned, navigate to the meetingsdk-angular-sample directory:

$ cd meetingsdk-angular-sample

Then install the dependencies:

$ npm install

Open the meetingsdk-angular-sample directory in your code editor.

Open the src/app/app.component.ts file, and enter values for the variables:

NEW: To use the Component View, replace app.component.ts with app-new.component.ts. (The leaveUrl is not needed). Also, remove the Client View CSS styles on lines 27 and 28 in in angular.json.

Variable	Description
authEndpoint	Required, your Meeting SDK auth endpoint that securely generates a Meeting SDK JWT. Get a Meeting SDK auth endpoint here.
sdkKey	Required, your Zoom Meeting SDK Key or Client ID for Meeting SDK app type's created after February 11, 2023. You can get yours here.
meetingNumber	Required, the Zoom Meeting or webinar number.
passWord	Optional, meeting password. Leave as empty string if the meeting does not require a password.
role	Required, 0 to specify participant, 1 to specify host.
userName	Required, a name for the user joining / starting the meeting / webinar.
userEmail	Required for Webinar, optional for Meeting, required for meeting and webinar if registration is required. The email of the user starting or joining the meeting / webinar.
registrantToken	Required if your meeting or webinar requires registration.
zakToken	Required to start meetings or webinars on external Zoom user's behalf, the authorized Zoom user's ZAK token. The ZAK can also be used to join as an authenticated participant.
leaveUrl	Required for Client View, the url the user is taken to once the meeting is over.
Example:

authEndpoint = 'http://localhost:4000'
sdkKey = 'abc123'
meetingNumber = '123456789'
passWord = ''
role = 0
userName = 'Angular'
userEmail = ''
registrantToken = ''
zakToken = ''
leaveUrl = 'http://localhost:4200'
Save app.component.ts.

Run the app:

$ ng serve --open

Usage
Navigate to http://localhost:4200 and click "Join Meeting".

Client View
Zoom Meeting SDK Client View

Component View
Zoom Meeting SDK Component View

Learn more about Gallery View requirements and see more product screenshots.

Deployment
The Angular Sample App can be easily deployed to GitHub Pages, or another static web hosting service, like an AWS S3 bucket.

GitHub Pages
Create a repo on GitHub.

Add the remote to your project:

$ git remote add origin GITHUB_URL/GITHUB_USERNAME/GITHUB_REPO_NAME.git

Open the angular.json file and replace the value for "baseHref" with your GitHub repo name surrounded by slashes like this: /GITHUB_REPO_NAME/. Example: "baseHref": "/GITHUB_REPO_NAME/"

Build your project:

$ ng build --prod

Git add, commit, and push your project:

$ git add -A

$ git commit -m "deploying to github"

$ git push origin master

On GitHub, in your repo, navigate to the "settings" page, scroll down to the "GitHub Pages" section, and choose the "master branch /docs folder" for the source.

Now your project will be deployed to https://GITHUB_USERNAME.github.io/GITHUB_REPO_NAME.

Other Static Web Hosting
Build your project:

$ ng build --prod

Deploy the complied /docs directory to a static web hosting service, like an AWS S3 bucket.

Advanced Deployment
For more advanced instructions on deployment, see the Angular Deployment docs.

Need help?
If you're looking for help, try Developer Support or our Developer Forum. Priority support is also available with Premier Developer Support plans.
