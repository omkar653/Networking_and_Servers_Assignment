Step 1 - First we will install nginx in our linux system using below commands - 

$ sudo apt update
$ sudo apt install nginx

Step 2 - Create directory to place the html file to be used as website content -

$ sudo mkdir /var/www/awesomeweb

Step 3 - create index.html file and put the html code -

$ cd /var/www/awesomeweb
$ sudo nano index.html

Step 4 - Create a server block configuration file with the name 'awesomeweb' in /etc/nginx/sites-available -

$ sudo nano /etc/nginx/sites-available/awesomeweb

Step 5 - Add below configuration to the file -

server {
        listen 80;

        server_name awesomeweb;

        root /var/www/awesomeweb;
        index index.html;

        location / {
                try_files $uri $uri/ =404;
        }
}

Step 6 - Create a symbolic link to 'sites-enabled' directory -

$ sudo ln -s /etc/nginx/sites-available/awesomeweb /etc/nginx/sites-enabled/

Step 7 - Restart nginx server

$ sudo systemctl restart nginx

Step 8 - Add the below line to /etc/hosts -
127.0.0.1   awesomeweb

Step 9 - go to 'http://awesomeweb' and check the website.
