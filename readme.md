# Laravel 5 Simple User Invitation using Mailable
-----
## Quick Start:

Clone this repository and install the dependencies. Kindly change your CUSTOM_DIRECTORY.

    $ git clone https://github.com/rootchips/user-invitataion-mailable.git CUSTOM_DIRECTORY && cd CUSTOM_DIRECTORY
    $ composer install
    
Rename the `.env.example` to `.env`, then create a database setting and mail server setting.

    $ mv .env.example .env
    $ vi .env

Edit the `.env` file and save.

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=yourdatabase
DB_USERNAME=yourid
DB_PASSWORD=yourpasswd
```

Try using mailtrap.io or Google Mail.

```
MAIL_DRIVER=smtp
MAIL_HOST=smtp.youremailprovider.com
MAIL_PORT=smtpport
MAIL_USERNAME=yourvalid@emailaddress
MAIL_PASSWORD=youremailpasswd
MAIL_ENCRYPTION=tls/ssl
```

Generate an application key and migrate the tables.

    $ php artisan key:generate
    $ php artisan migrate

You can see the migrated tables in your database.

Finally, serve the application.

    $ php artisan serve

Open [http://localhost:8000](http://localhost:8000) from your browser. 
To send user invitation, hit the link 
[http://localhost:8000/invite](http://localhost:8000/invite) from your browser.
You must send valid user's email address. 

## License

This is free software distributed under the terms of the MIT license

-----
