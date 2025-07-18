# On-Prem DB Training
Slides are available in the [Google drive](https://docs.google.com/presentation/d/1cYpzJD4RtvUL_j3t3jDAhAp3ZIA1qdiwL2-FQSauxjQ/edit?usp=sharing).
This demo uses docker-compose to run a local deployment of Odoo, MailHog, and Nginx on port 80.

## How to run
1.  Install and run the Docker Engine and Docker Compose. I recommend installing via [Docker Desktop](https://docs.docker.com/get-started/get-docker/), which includes both tools (no sign in is necessary).
The Ubuntu-specific instructions are available [here](https://docs.docker.com/desktop/setup/install/linux/ubuntu/).
2.  Clone this repo and cd into `docker_demo`.
3.  Edit "`<YOUR ENTERPRISE DIRECTORY>`" in `compose.yml` to point to your Odoo enterprise source folder.
4.  [Optional] Pre fetch the images by running `docker compose pull`
5.  Launch the demo by running `docker compose up`. You should see four containers get spun up. The instance can be gracefully stopped by entering Ctrl+C in the terminal or by hitting the stop button from Docker Desktop.
<img width="610" height="254" alt="image" src="https://github.com/user-attachments/assets/924e0feb-c2fc-4280-9090-89cfe57c66a1" />

6.  Navigate to `odoo.localhost` and you should be directed to the database manager where you can restore `db_dump.zip`. The MailHog instance is available at `mailhog.localhost`
