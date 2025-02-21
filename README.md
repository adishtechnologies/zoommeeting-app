**Angular App**

URL: http://localhost:4200/
This application includes a component that launches the Zoom app directly within the Angular page.
The genSignature method is used to generate the signature based on the user role:
Role = 0 → Launches the app for a student.
Role = 1 → Launches the app for a host.

**Node App**

URL: http://localhost:3000/
Integrated with the Marketplace Developer App, including a callback URL.
Developer app details are stored in environment variables for both applications.
No further changes are needed in the Marketplace app until it's ready for production.

**Access Token for Developer Testing**
Use the following URL to generate a new access token (expires in one hour):
http://localhost:3000/api/zoom-auth
