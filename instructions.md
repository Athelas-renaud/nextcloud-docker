Step 0 : Ensure your DNS points to your wanted server
1. Those are instructions based on Ubuntu server:
2. Ensure you have installed *Docker-compose nginx certbot*
2. Copy the **nextcloud.conf** file into **/etc/nginx/sites-enabled.conf**
4. Copy the **docker-compose.yml** file somewhere and execute: `docker-compose up -d`
5. verify nginx is happy with `nginx -t` and `nginx -s reload`
6. Launch `certbot --nginx` and accept that it changes your conf files
7. Proceed to install your nextcloud going into https://yourserver.com
8. Inside your **nextcloud container** :
9. Modify **/var/www/html/config/config.php** with `"overwriteprotocol" => "https",` Don't forget the ","
10. (this will allow to use the nextcloud PC client)
11. Enjoy