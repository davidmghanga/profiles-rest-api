# Profiles REST API

This is a REST API built using Python, Django, Django REST Framework, Virtual Box, Vagrant and ModHeader Chrome Extension.

This is a fully functioning REST API that can handle:
- Creating and updating user profiles.
- Login and authentication.
- Posting status updates.
- Viewing status update feeds.

# Local Development
### Running the project
This project runs using Vagrant. It should work consistently on Windows, MacOS and Linux machines. Follow the steps below to run a local development environment.
1. Ensure you have Virtual box and Vagrant installed. You can download Virtualbox from https://www.virtualbox.org/ and Vagrant from https://www.vagrantup.com/
2. Clone the project, cd to it in the Terminal/Command Prompt and run the following command to download and set up the vagrant server:
   ```sh
   vagrant up
   ```
3. Connect to the vagrant server:
   ```sh
   vagrant ssh
   ```
4. Switch to the vagrant directory:
   ```sh
   cd /vagrant
   ```
5. Create Python virtual environment:
   ```sh
   python -m venv ~/env
   ```
6. Activate the virtual environment:
   ```sh
   source ~/env/bin/activate
   ```
7. Install Python dependencies in the virtual environment:
   ```sh
   pip install -r requirements.txt
   ```
8. Make migrattions to set up and sync Database:
   ```sh
   python manage.py migrate
   ```
9. Create a super user to log into Django Admin:
    ```sh
    python manage.py createsuperuser
    ```
10. Start the developement server:
    ```sh
    python manage.py runserver 0.0.0.0:8000
    ```
12. Access the Djangp Admin at http://127.0.0.1:8000/admin/
13. Log into the Django Admin with you superuser email and password.
14. Access the Profiles API Viewset at http://127.0.0.1:8000/api/profile/
15. Access the login API Viewset at http://127.0.0.1:8000/api/login/
16. To create authentication token, log into the login API Viewset at http://127.0.0.1:8000/api/login/ with your superuser credentials.
17. Copy the token value inside the double quotes, open the ModHeader extension and write Authorization in the name field, then in the Value field, write Token, then add space and paste the token value copied earler. Check the checkbox to enable authorization.
18. Access the Feed API at http://127.0.0.1:8000/api/feed/
19. Access the API Viewset at http://127.0.0.1:8000/api/hello-viewset/
20. Access the API View at http://127.0.0.1:8000/api/hello-view
### Quiting the developement server
1. Press Control + C on Windows and Linux or Command + C on MacOS.
2. Deactivate the Python virtual environment:
   ```sh
   deactivate
   ```
3. Exit the Vagrant server:
   ```sh
   exit
   ```

    
   
