# Dockerizing Laravel and MySQL App with Ansible

This repository provides an example of how to Dockerize a Laravel and MySQL application and automate the deployment process using Ansible.


[![Product Name Screen Shot][product-screenshot]](https://example.com)

[![Product Name Screen Shot][route-screenshot]](https://example.com)

## Prerequisites

Before getting started, ensure that you have the following installed:

- Docker
- Docker Compose
- Ansible

## Dockerizing the Laravel and MySQL App

To Dockerize the Laravel and MySQL app, follow these steps:

1. Clone this repository:
   ```sh
   git clone https://github.com/Francismensah/npontu-devops-assignment.git
   ```
2. Navigate to the cloned repository:
   ```sh
   cd npontu-devops-assignment
   ```

3. Update the Laravel configuration:
- Modify the Laravel application's `config/database.php` file to use the MySQL container as the database.
- Set the `DB_HOST` value to the MySQL service name defined in the `docker-compose.yml` file, which is "db" in this example.
- Update other necessary configuration values, such as `DB_USERNAME`, `DB_PASSWORD`, etc.

4. Build and start the Docker containers:

   ```sh
   docker-compose up --build
   ```
5. Wait for the containers to be built and started. Once complete, you should be able to access the Laravel application in your browser at `http://localhost:8000`.

## Running the Ansible Playbook

To automate the deployment process using Ansible, follow these steps:

1. Ensure that you have Ansible installed on your local machine.

2. Update the inventory file:
- Replace inventory.ini with your inventory file, which contains the target hosts (e.g., webserver) where the deployment should take place.
- Replace the `webserver` host with the IP address or hostname of the target server where you want to deploy the application.
- Save the changes.

3. Update the Ansible playbook:
- Open the `playbook.yaml` file in a text editor.
- Customize the playbook as per your specific deployment requirements if needed.
- Save the changes.

4. Run the Ansible playbook:


This command will execute the playbook and automate the deployment of the Laravel application to the target server.

5. Wait for the Ansible playbook to complete the deployment process.

Once the Ansible playbook finishes executing, the Laravel application should be successfully deployed on the target server.

## Additional Notes

- Ensure that the necessary ports (e.g., 8000 for Laravel, 3306 for MySQL) are open and accessible.
- Make sure to update any environment-specific configurations (e.g., database credentials, container names) as required.

That's it! You have successfully Dockerized the Laravel and MySQL app and automated the deployment process using Ansible. Enjoy running your Laravel application in a containerized environment.

Feel free to reach out if you have any questions or encounter any issues.