# Odoo
This repo includes some of the main files used for working with Odoo. Mainly related to Docker implementation for Odoo which is a better way to deploy this software package.

# How to implement and manage Odoo with Docker
1. Install Docker from official webpage: https://www.docker.com/products/docker-desktop
2. Install Kitematic as the client toolbox for easier the management of Docker: https://kitematic.com/
3. Use the file docker-compose.yml and verify if current configuration of Odoo release and Database admin is OK for you.
4. Using the console/PowerShell, go to the archive directory and execute *docker-compose up -d *
5. Verify the execution with *docker ps*
6. Verify the current processor/memory consumption with *docker stats*
7. Connect to pgadmin with http://localhost:5051/browser and create a new Server with hostname *db*, port *5432*, user *odoo*, password *the-one-defined-in-odoo.conf*.
8. You could use the Kitematic client to verify the current execution status of the containers and control the start/reset/stop for each one.
9. After all 3 containers: odoo_docker_db, odoo-docker_pgadmin and odoo-docker_odoo are up, you could access Odoo with the address: http://localhost:8069. To select the databese the address is: http://localhost:8069/web/database/selector.
