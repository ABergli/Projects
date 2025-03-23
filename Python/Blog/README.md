# Blog and Vlog Application

This project involves building a Blog and Vlog application using Django, a Python web framework. The application allows users to create, edit, and delete posts, including textual, image, and video content.

## Project Overview
- **Purpose:** To create a web-based platform for managing blog and vlog posts.
- **Framework:** Django (Python).

## Features
1. **Post Management**:  
   - Create, edit, and delete posts.
   - Support for text, images, and videos.  

2. **Model Design**:  
   The application includes a structured model with the following fields:  
   - `title`: Post title (text).  
   - `author`: Post author (text).  
   - `updated_on`: Last updated date/time.  
   - `content`: Main content (text).  
   - `created_on`: Creation date/time.  
   - `image`: Image upload.  
   - `video`: Video upload.  

3. **Admin Interface**:  
   - User authentication through Django's built-in admin system.  
   - Add, edit, and manage posts easily via the admin interface.  

4. **Deployment**:  
   The project was deployed on **Amazon Web Services (AWS)**, providing easy access to the application,
   but has been taken down. The code base is here.  

## Implementation Steps
1. **Set Up the Django Project**:  
   - Follow Django's guidelines for creating a new project and app.

2. **Database Migrations**:  
   - Create database migrations for the model fields.  

3. **Development**:  
   - Customize `view.py`, `url.py`, and template files to implement functionality.  

4. **Admin Panel Configuration**:  
   - Add models to the admin interface and set up user login credentials.  

5. **Deployment**:  
   - Host the application on AWS and ensure the deployment is working properly.  

## Outcome
This project showcases the use of Django for creating a dynamic application that handles both textual and multimedia posts. The final deployed platform allows users to manage and interact with blog and vlog content seamlessly.



