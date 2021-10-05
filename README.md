# bannerbear-insomnia-config
Configuration file for Insomnia.rest API tool

## Before installing

This config is dependent on you having some test data in your Bannerbear account already. So for testing purposes via the Bannerbear web-based API console create:

1. At least one image template, and one image
2. At least one template set, and one collection
3. At least one video template, and one video

You are now ready to fire requests from Insomnia.

## How to Install

1. Download or clone this repo locally
2. Create a file named `keys.env` - use the same template and add your own API key
3. Install [Insomnia](https://insomnia.rest/)
4. Install the dotenv plugin and follow the instructions in (2) [here](https://konghq.com/blog/avoiding-plain-text-passwords-insomnia/): `insomnia-plugin-dotenv`
5. In Insomnia under *Manage Environments* ensure that the API Key is being correctly pulled from your `keys.env` file

![Screenshot 2021-10-05 at 09 02 49](https://user-images.githubusercontent.com/30496/135944402-592bf522-b7ff-46ba-841d-89ea4b2586ca.png)

You can now run API requests and should see the following selection of endpoints:

![Screenshot 2021-10-05 at 09 04 18](https://user-images.githubusercontent.com/30496/135944510-6ff65dd6-f23d-4cde-a0c0-5b17c674d1a5.png)

## About Dynamic Variables

There are no hard-coded object IDs in this config. This Insomnia setup uses cascading data from previous requests. So for example, in order to send the "Create an Image" request you will first need to send the "List all Images" request, in order to load variables into the Insomnia environment.