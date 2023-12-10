# MVC-Tech-Blog

Week-14 Challenge (Model-View-Controller)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](code_of_conduct.md)

## Table of Contents

- [Description](#description)

- [Screenshots](#screenshots)

- [Technologies-Used](#technologies-used)

- [Installation](#installation)

- [Features](#features)

- [Usage-Information](#usage-information)

- [Suggested-Future-Development](#suggested-future-development)

- [License](#license)

## Description


Rewording the application description:
This full-stack application offers a platform for tech enthusiasts to create, share, and discuss industry-related content. Users can store their creations in a personalized dashboard, engage with other users' posts through comments, and manage their own content through editing and deletion options.

The application prioritizes user security. While exploring the public homepage requires no account, authentication via session storage and cookies is implemented for accessing the dashboard, creating or viewing specific posts, and ensuring profile protection. Passwords are securely hashed using the bcrypt dependency before storing them in the MySQL database.

The project utilizes a robust architecture with MVC structure, Sequelize ORM for seamless front-end/database interaction, and Express routing for efficient navigation. Additionally, the Handlebars templating engine facilitates dynamic data rendering, simplifying front-end development and promoting code reuse.

Developing this application presented several challenges, including mastering the Handlebars templating engine for effective data manipulation and overcoming routing and middleware syntax intricacies. As my first full-stack project, managing numerous files and understanding the complex interactions between various components initially felt overwhelming. However, perseverance and dedication led to a successful outcome, resulting in this fully functional web application.

## Screenshots
![MVC 1](<Image/Screenshot.PNG>) 

![MVC 2](<Image/Screenshot1.PNG>)

## Technologies Used

Node.js (v16.19.1), Express.js (v.14.18.2), JavaScript, MySQL, Sequelize (ORM), and Handlebars (template engine). It utilizes the node package manager (npm) dependencies sequelize (v6.31.1), mysql2 (v3.3.0), express (v4.18.2), dotenv (v16.0.3), nodemon (v2.0.22), bcrypt (v.5.1.0), bootstrap (v5.2.3), connect-session-sequelize(v.7.1.6), express-handlebars (v7.0.7), and express-session (v1.17.3). Jest (v.29.5.0) is installed for future unit testing. Also, the Insomnia application was utilized to test the functionality of routes within the program.

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
![NPM](https://img.shields.io/badge/NPM-%23CB3837.svg?style=for-the-badge&logo=npm&logoColor=white)
![Sequelize](https://img.shields.io/badge/Sequelize-52B0E7?style=for-the-badge&logo=Sequelize&logoColor=white)
![Nodemon](https://img.shields.io/badge/NODEMON-%23323330.svg?style=for-the-badge&logo=nodemon&logoColor=%BBDEAD)
![Bootstrap](https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white)
![Jest](https://img.shields.io/badge/-jest-%23C21325?style=for-the-badge&logo=jest&logoColor=white)
![Insomnia](https://img.shields.io/badge/Insomnia-black?style=for-the-badge&logo=insomnia&logoColor=5849BE)

## Installation

1. Clone the repo:
   git clone https://github.com/Donsidious/MVC-Tech-Blog

2. Open in VS Code. If you do not have VS code you must install it.

3. Using the terminal, install node.js v16. If you have homebrew, the command should look like the following (brew install node@16), however this may vary and the documentation should be consulted.

4. Once node.js v16 is installed, in the terminal, utilize the command npm init -y to initialize and create a package.json where project files will be stored.

5. Next, use the terminal to run the command npm i to install the dependencies associated with this application (developers may need to install dependencies directly from the command line).

   Commands to install each dependency:

   - Command for sequelize will be npm i sequelize
   - Command for mysql2 will be npm i mysql2
   - Command for express will be npm i express@4.18.2
   - Command for dotenv will be npm i dotenv
   - Command for nodemon will be npm i nodemon
   - Command for bcrypt will be npm i bcrypt
   - Command for bootstrap will be npm i bootstrap
   - Command for connect-session-sequelize will be npm i connect-session-sequelize
   - Command for express-handlebars will be npm i express-handlebars
   - Command for express-session will be npm i express-session
   - Command for jest will be npm i jest

6. Following this, it's essential to ensure that you've included an .env file in the main directory of your repository. Inside this file, you should set your environmental variables, including the database name, your MySQL username, and your MySQL password. This step must be done before launching the application and will enable the connection.js file to access your environmental variables, ensuring the security of your sensitive information.

7. If you do not have a MySQL account, you will need to create one (see https://dev.mysql.com/doc/mysql-installation-excerpt/5.7/en/).

8. Once you've successfully installed all the dependencies, the next step is to create the database. To do this, navigate to the "db" directory, which contains the "schema.sql" file. Afterward, open a MySQL shell by executing the command `mysql -u root -p`. You will be prompted to enter your password. Once your password is entered, you will gain access to the MySQL shell.

9. Once in the MySQL shell you will then run the command source schema.sql. This will create the database.

10. After successfully creating the database, the next step is to seed it, which will also generate the model structure for the database tables. To achieve this, navigate to the root directory and execute the command `npm run seed`. It's essential to run this command from the root directory since the .env file is located there.

11. Once the database has been seeded, you will then be able to run the command npm start from the root directory to spin up the server. With nodemon installed, you will also be able to utilize the command npm run watch to keep the server spun up between code edits.

12. From there, you can utilize applications such as Insomnia to test the functionality of the routes within the program and make edits to both the front-end and back-end of the code base.

## Features

This application boasts several key features:

1. **User Account Creation:** Users can create an account, and their login information is securely hashed and stored in a database.

2. **Login Validation:** Users can log in later using their hashed credentials, which are validated during the login process, ensuring secure access.

3. **Public Access:** Visitors can access the homepage or public feed without needing to create an account, promoting inclusivity.

4. **Account Prompt:** When attempting to access specific blogs or create posts, visitors will be prompted to create an account, encouraging engagement.

5. **Dashboard:** Registered users have access to a dashboard, providing them with a space to manage and store their own created content.

6. **Interaction:** Users can interact with other users' posts by leaving comments, fostering engagement and community-building.

7. **Content Management:** Registered users have the ability to edit and delete their own posts, giving them control over their content.

These features collectively enhance the user experience and make the application versatile for both visitors and registered users.

## Usage Information

Users interact with the application exclusively through the frontend user interface. They start by seeing a public feed and have the option to log in or create an account through a clear button prompt. After this, they can seamlessly navigate the entire application, including creating content and engaging with other users, without encountering any significant hurdles or complexities. The design prioritizes a user-friendly experience.

## Suggested Future Development

- Continued UI development
- Addition of a search feature
- Addition of a like feature
- Addition of a trending feature
- Addition of a friends feature
- Addition of a profile picture feature

## License

NOTICE: This application is covered under the MIT License

