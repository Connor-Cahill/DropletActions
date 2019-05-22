# Droplet Actions CLI
Helping you take the headache out of deploying projects to Digital Ocean Droplets.
> You did the thing once, why do it again?
## Overview
Droplet Actions is a CLI built to simplify the process of shipping web apps to/managing Digital Ocean Droplets. 
This CLI removes the need for you to:

- Navigate to the Digital Ocean dashboard to manage droplets
- SSH into droplet to set it up tools such as docker & docker-compose
- SSH into droplet to clone repositories/setup environment variables to deploy projects

DropletActions lets you handle the process of creating Droplets, setting up Droplets with proper dev tools, cloning your repos & environment variables over to your VPS.

This can take an annoying process that requires using the Digital Ocean GUI and ssh-ing into the Droplet.


## Installation/Setup


## Usage
Once the CLI is installed and setup you should be able to use it in your terminal freely.
You will always start with the top level command "dropletactions" the specify command and arguments:

        $ dropletactions <COMMAND> <ARGS>


*Note: go to the Command section for a list of arguments for each command.*

## Commands
This section breaks down the current available commands and specifies arguments that must be passed for each

### Create
This command creates a fresh DO Droplet. Note this command creates Droplet with lots of default settings at this point. 
Things to note:

- Droplet automatically created on $5/month plan
- Uses defualt Ubuntu image
- Connects all SSH Keys on your DO account to new droplet
- Sets region to "sfo2" (San Francisco 2)
- IPv6 is false
- Backups are false 

Although I would like to make these all inputs in the future it currently builds the cheapest option with no other bells or whistles.<br>
<br>
**Arguments:**
- Droplet Name<br>
<br>

**Example Use:**

        $ dropletactions create my-new-droplet

### List
The list command lists out all of your Droplets:
- name
- ID
- Public IP
<br>
*note: pagnation is not setup yet and the list command will return at most 20 Droplets*
<br>
This command is useful for when you need to pass a Droplets Public IP or ID through another command as an argument.
**The list command does not take any arguments.**
<br>
**Example Use:**

        $ dropletactions list


