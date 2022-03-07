#Hello World Site!

## What

This repository showcases a simple scenario for a Blue / Green deployment with little to no downtime. The following services have been mocked for the sake of this exercise;

 - Instead of using SSH to connect to a remote machine, we'll be using docker to mimic a runtime system (deployment server with nginx). For this a standard nginx image will be used
 - We will assume that a third-part is responsible for development and maintenance of the site and only make the files available to us through a shared folder (might even be via SFTP)
 - Since we're assuming that the docker container is a server running on a remote machine, `docker copy` and `docker exec` will represent `scp` and `ssh` respectively.
 - Only the latest version of the website is committed to git (replaced)

## Structure

The repository includes the following main folders and/or files;

- `.github` - Includes GitHub files like workflows that execute based defined git/GitHub events
- `site` - The current state of our website (the live website version) on a remote server
- `next` - Latest website in a form of a zip