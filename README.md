# InfraGIT
## A SaaS secure VCS (based on Git) for confidential repositories. 

#### How to setup this program:
***
1. Make sure you are connected to internet
2. This repo uses `make` to automate build. Make sure to install it. [For Debian(Ubuntu), apt-get install make]
3. Clone this repo or download it.
   * To clone this repo: `git clone https://github.com/AshirwadPradhan/infragit`
   * To download the zip: [Download](https://github.com/AshirwadPradhan/infragit/archive/master.zip)
        * Extract the downloaded zip to `infragit`   
4. Navigate to the directory `cd infragit`
5. Activate `virtualenv`
     * Install virtualenv using `pip3 install virtualenv`. (replace pip3 with pip if using windows)
     * Make a virtual env. `virtualenv env`
     * Activate the virtual env. `source env/bin/activate`
6. Prepare the environment `make prepare-dev`
    * When prompted for a password enter `this`
7. Run the server `make run-server`
    * When prompted for a password enter `this`
8. Now open a different terminal , navigate into the folder `infragit` and run `make run-client` to run the client
9.  Now your can use the client for different tasks.
10. Example 1. Register a user, login and create a repo.
    * > `register user` It will prompt for a password enter your desired password.
    * > `login user` Enter the password when asked for
    * > `creater a` To create a repo with name 'a'
    * > `logout user` To logout of that account
11. Example 2. Pushing and Pulling from a remote repo.
    * > `pushr a` Push local changes of repo 'a' to remote
    * > `pullr a` Pull remote changes of repo 'a' to local

##### Note :- Add CA's public key to Trusted Root Certificates if you face any 'Invalid CA certificate' issue (required for Microsoft Windows 10)


<!-- ##### Run Server : `uwsgi --master --https localhost:5683,server-public-key.pem,server-private-key.pem --mount /=gateway:app`
 --Enter secret for server private key when asked -->