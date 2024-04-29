<h1 align="center" id="title">Backend Task (Wasserstoff)</h1>

<p align="center"><img src="https://socialify.git.ci/sanjidrahman/wasserstoff-BackendTask/image?font=Source%20Code%20Pro&amp;language=1&amp;name=1&amp;owner=1&amp;pattern=Formal%20Invitation&amp;theme=Dark" alt="project-image"></p>

<h2>🚀 Demo</h2>

[http://localhost:5050](http://localhost:5050)

  
  
<h2>🧐 Features</h2>

Here're some of the project's best features:

*   Authentication and Authorization system
*   Utilised mongoose for schema creation and validation
*   Bcrypt for ecrypting user credentials
*   Review and approval of images
*   Restricting access of users by admin
*   Image storing in S3 Bucket
*   Auto annotations using AWS Rekognition

<h2>🛠️ Installation Steps:</h2>

<p>1. Clone project</p>

```
https://github.com/sanjidrahman/wasserstoff-BackendTask.git
```

<p>2. Install dependencies</p>

```
npm install
```

<p>3. Setup .env file</p>

```
link to the env 
```

<p>4. Start project</p>

```
npm start
```

  
  
<h2>💻 Built with</h2>

Technologies used in the project:

*   Nodejs (Expressjs)
*   MongoDB
*   JWT
*   Multer
*   Mongoose
*   AWS S3 Bucket
*   AWS Rekognition

<h2>🔗 Routes and Descriptions</h2>

### Users
* `POST /signup` - User sign-up.
* `POST /login` - User sign-in.
* `POST /upload` - Handles user-uploaded image and returns annotations. (Use 'file' as the key to upload file)

### Admin
* `POST /admin/signup` - Admin sign-up.
* `POST /admin/signin` - Admin sign-in.
* `PATCH /admin/block/:id` - Block user access. (Replace ':id' with the user's _id)
* `PATCH /admin/block/:id` - Unblock user access. (Replace ':id' with the user's _id)
* `GET /admin/userimages/:id` -  Retrieve all images uploaded by a specific user. (Replace ':id' with the user's _id)
* `GET /admin/users` -  Retrieve all users.
* `GET /admin/images` - Retrieve all uploaded images.
* `GET /admin/image/:id` -  View details of a specific image. (Replace ':id' with the image's _id)
* `PATCH /admin/approve/:id` - Approve an image after reviewing annotations. (Replace ':id' with the image's _id)
* `PATCH /admin/reject/:id` -  Reject an image after reviewing annotations. (Replace ':id' with the image's _id)
* `GET /admin/export` - Export approved images in the desired format. (Specify format as a query parameter, e.g., /admin/export?format=csv)
* `GET /admin/export/:id` - Export annotations of a particular image in the desired format. (Specify format as a query parameter, e.g., /admin/export/<id>?format=csv)