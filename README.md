## Running the Application

To run the application locally, follow these steps:

1. Clone the repository to your local machine:

$ git clone https://github.com/nineshots109/CS120_Project2.git
$ cd CS120_Project2


2. Initialize a virtual environment:
- Windows:
  ```
  $ python3 -m venv venv
  $ venv\Scripts\activate.bat
  ```
- Unix/MacOS:
  ```
  $ python3 -m venv venv
  $ source venv/bin/activate
  ```
Then you have to Add Environment Variables
Create a file called config.env that contians the secret key. Very important: do not include the config.env file in any commits. This should remain private. You will manually maintain this file locally, and keep it in sync on your host.

Variables declared in file have the following format:

In order for Flask to run, there must be a SECRET_KEY variable declared. Generating one is simple with Python 3:

$ python3 -c "import secrets; print(secrets.token_hex(16))"
This will give you a 32-character string. Copy this string and add it to your config.env:

SECRET_KEY=Generated_Random_String

3. Install the dependencies:
$ pip install -r requirements.txt


4. Install other necessary dependencies:

   Before that, type "sudo apt-get update"

For Sass:

  $ gem install sass

Then Redis:
  - Mac: $ brew install redis
  - Linux: $ sudo apt-get install redis-server
  

5. Create the database:
$ python manage.py recreate_db

6. Run the app:
$ source env/bin/activate
$ honcho start -e config.env -f Local


7. Open your web browser and navigate to [http://localhost:5000](http://localhost:5000) to view the application.

These instructions will set up and run the Flask application locally on your machine, allowing you to access it through your web browser.
