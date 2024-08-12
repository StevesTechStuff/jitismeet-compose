Jitsi Meet docker compose file with Nginx Proxy Manager and MariaDB

Download and extract the latest release. DO NOT clone the git repository. See below if you are interested in running test images:

wget $(curl -s https://api.github.com/repos/jitsi/docker-jitsi-meet/releases/latest | grep 'zip' | cut -d\" -f4)

Unzip the package:

unzip <filename>

Create a .env file by copying and adjusting env.example:

cp env.example .env

Set strong passwords in the security section options of .env file by running the following bash script

./gen-passwords.sh

Overwrite extacted docker-compose.yml with this one.

docker compose up -d

Setup the proxy at http://serverip:81
