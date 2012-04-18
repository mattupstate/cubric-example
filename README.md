# Cubric Example Application

This Flask/WSGI application illustrates how to use Cubric for deployment. Perform the following steps to create a server and deploy the application:

### 1. Clone the repository

    $ git clone git://github.com/mattupstate/cubric_example.git
    $ cd cubric_example

### 2. Install Cubric

    $ pip install https://github.com/mattupstate/cubric/tarball/develop

### 3. Copy the sample rcfile for the provider you wish to use

Replace `<provider>` with either `ec2` or `rackspace`

    $ cp rcfile.<provider>.sample rcfile.<provider>

### 4. Modify the rcfile values to match those of your AWS or Rackspace account

### 5. Create the server and deploy the application in one line

Replace `<provider>` with either `ec2` or `rackspace`:

    $ fab -c rcfile.<provider> create_server create_app_context deploy

### 6. Open the public DNS or IP address in your browser!
