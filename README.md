# bannerbear-insomnia-config
Configuration file for Insomnia.rest API tool

Steps to use:

1. Download or clone this repo locally
2. Create a file named `keys.env` - use the same template and add your own API key
3. Install [Insomnia](https://insomnia.rest/)
4. Install the dotenv plugin and follow the instructions in (2) [here](https://konghq.com/blog/avoiding-plain-text-passwords-insomnia/): `insomnia-plugin-dotenv`
5. In Insomnia under *Manage Environments* ensure that the API Key is being correctly pulled from your `keys.env` file

![Screenshot 2021-10-05 at 09 02 49](https://user-images.githubusercontent.com/30496/135944402-592bf522-b7ff-46ba-841d-89ea4b2586ca.png)

You can now run API requests.

![Screenshot 2021-10-05 at 09 04 18](https://user-images.githubusercontent.com/30496/135944510-6ff65dd6-f23d-4cde-a0c0-5b17c674d1a5.png)

Note that this config uses variables that rely on response data of previous requests. Example: to run "Create an Image" you will need to run the "List all Images" request first, as "Create an Image" uses a template ID picked up from "List all Images".

Therefore, in order to use this config you will need to have some pre-existing data in your Bannerbear account.
