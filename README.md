# Assignment
#Level 1

""" There is many to many relationships between students and teachers.Store their data in the tables.
if a teacher is selected the corresponding students will be displayed and
if the students are selected then the corresponding teachers should be displayed"""
#Create a new Django project and app
#Define your models in models.py of your app (e.g., myapp/models.py)
#Create and apply migrations to create the database tables
"""Now, you can use the Django admin site to add students and teachers and create many-to-many relationships between them.
    To do so, register these models in the admin.py file (e.g., myapp/admin.py):"""

"""Create views and templates to display students for a selected teacher and teachers for a selected student.
For example, create a view in views.py (e.g., myapp/views.py) and corresponding templates:"""

"""Create corresponding HTML templates (students_for_teacher.html and teachers_for_student.html) to display the data."""
#Create URLs for these views in your app's urls.py (e.g., myapp/urls.py)
"""Now, you can access the views you created to display students for a selected teacher and teachers for a selected student.
Make sure to configure your project's settings, including the INSTALLED_APPS, database settings, and static files, as per your project requirements."""

#Level 2

#Choosing the teacher and a student pair. Generate the certificate
"""Create a new view that allows you to choose a teacher and student pair and generate a certificate.
You can create a new view in your app's views.py (e.g., myapp/views.py) as follows:"""

"""Create templates for the views. You'll need two templates:
one for choosing the teacher and student pair (generate_certificate.html) and another for rendering the certificate (certificate.html).
Create these templates in your app's templates directory.generate_certificate.html:"""

#certificate.html
"""<!DOCTYPE html>
<html>
<head>
    <title>Certificate</title>
</head>
<body>
    <h1>Certificate</h1>
    <p>This is to certify that {{ student.name }} has successfully studied under the guidance of {{ teacher.name }}.</p>
</body>
</html>"""

"""Finally, make sure you have the appropriate URLs configured in your project's urls.py as shown in the previous answer.
Now, when you visit the /generate_certificate/ URL, you will see a form where you can choose a teacher and a student.
When you submit the form, it will generate and display the certificate based on the selected teacher and student pair.
you can further customize the certificate template to meet your specific needs."""

#level 3 -Verify the certificate using the JWT token

#Install the PyJWT library if you haven't already. You can install it using pip:
pip install PyJWT

"""Create a function in your Django app to generate JWT tokens for certificates.
You can do this by using a secret key and encoding the data you want to include in the token.
For example, you might want to include information about the student, teacher, and certificate expiration date."""

#Replace 'your_secret_key' with a secure secret key.

# Next, create a view in your Django app to verify certificates using the JWT token. In this view, you'll decode the token and validate it.
#Make sure to replace 'your_secret_key' with your actual secret key.

#Create a URL pattern in your app's urls.py to map the verify_certificate view:

"""You can now access the verify_certificate view by providing a valid token as part of the URL, like /verify_certificate/<token>.
This view will verify the certificate and return certificate details if it's valid."""
