# Documentation of Nutri project
<img src="https://i.imgur.com/twMrvzK.png" width="100">  

## Introduction
What is Nutri? Nutri is a smart nutrition planning tool designed to help users to eat heatlhier and cheapier. This project was made during Vilnius University Bachelor's degree's of Information Systems Engineering course of Computer's Architecture course. This guide is designed to help you, the reader, to try to make something simillar yourself. This project covers:
* Responsive web design technologies
* React.js framework
* Mysql databases
* Golang programming language
* REST API
* Docker
* AWS + Jenkins

So go ahead and make something cool too!

## Front-End crash course
This crash course is designed for developers, who want to learn how to start coding web-based apps. The course covers topics from basic HTML to React.js JavaScript library. If you are familliar with some topics, feel free to skip them and go to more advanced ones.

Before you start, don't forget to pick a text editor of your choice. There are plenty of good ones but I suggest you to grab my favorite - [Visual Studio Code](https://code.visualstudio.com/).

### Basic HTML / CSS
1) [Basic HTML syntax](https://www.w3schools.com/html/html5_syntax.asp)
2) [Basic CSS](https://www.w3schools.com/css/css_syntax.asp)
3) [HTML Course](https://www.codecademy.com/learn/learn-html)
4) [More CSS](https://medium.freecodecamp.org/want-to-learn-css-heres-our-free-20-part-course-9fb3dcb0a971)
5) [What is a Bootstrap?](http://getbootstrap.com/docs/4.1/getting-started/introduction/)
6) [Bootstrap Course](https://scrimba.com/g/gbootstrap4)
7) [More about the grid...](https://www.w3schools.com/bootstrap4/bootstrap_grid_system.asp)

### JavaScript
1) [Introduction to JS](https://www.codecademy.com/learn/introduction-to-javascript)
2) [More about ES6](https://www.tutorialspoint.com/es6/)
3) [Full Basic HTML/CSS/JS Course](https://learn.freecodecamp.org/)

### Quick note before continuing
Next you will meet with React.js library. Before you continue, I highly recommend you to install Node.js & npm into your PC. You can find the latest LTS version [here](https://nodejs.org/en/)

### React.js
1) [Meet the React!](https://reactjs.org/tutorial/tutorial.html)
2) [One of the best React.js courses](https://www.codecademy.com/learn/react-101)

### Before flying to the moon 🚀...
After you completed this crash course feel free to build whatever you want. If you need project ideas, I have some:
* [Chatbot](https://medium.freecodecamp.org/how-to-build-a-react-js-chat-app-in-10-minutes-c9233794642b)
* [Your portfolio site](https://medium.com/technoetics/create-a-developer-portfolio-using-reactjs-d34ea1bfb18e)

## Mysql Databases
This paragraph is wiretten to make you familiar with SQL language and Mysql stuff.

### What is SQL?
SQL (pronounced "ess-que-el") stands for Structured Query Language. SQL is used to communicate with a database. According to ANSI (American National Standards Institute), it is the standard language for relational database management systems. SQL statements are used to perform tasks such as update data on a database, or retrieve data from a database. Some common relational database management systems that use SQL are: Oracle, Sybase, Microsoft SQL Server, Access, Ingres, etc. Although most database systems use SQL, most of them also have their own additional proprietary extensions that are usually only used on their system. However, the standard SQL commands such as "Select", "Insert", "Update", "Delete", "Create", and "Drop" can be used to accomplish almost everything that one needs to do with a database.

### What is Mysql?
MySQL is a database management system. A database is a structured collection of data. It may be anything from a simple shopping list to a picture gallery or the vast amounts of information in a corporate network. To add, access, and process data stored in a computer database, you need a database management system such as MySQL Server. Since computers are very good at handling large amounts of data, database management systems play a central role in computing, as standalone utilities, or as parts of other applications.

### How to set up one?
Well I hope that you are using Ubuntu. If you don't, please do, because the following tutorial is written only for superior Linux users :). The short version of the installation is simple: update your package index, install the ```mysql-server package```, and then run the included security script.  
```bash
$ sudo apt-get update
$ sudo apt-get install mysql-server
$ mysql_secure_installation
```
If you want the longer guide go ahead [here](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-16-04)

## Go Golang!
Why Golang? It runs fast! Really fast! This programming language is easy to write, easier to maintain. Its syntax is really close to C++ or C, so it won't be hard for you to learn how to write in this cool language. I can write a long poem about "Why Go Works?" but [this guy](https://medium.com/@kevalpatel2106/why-should-you-learn-go-f607681fad65) did it better. So go ahead and read it! If you want to lear to write in Go, [this tutorial](https://tour.golang.org/welcome/1) is best in the internet. I highly recommend it:

## What is REST?
A RESTful API is an application program interface (API) that uses HTTP requests to GET, PUT, POST and DELETE data.
A RESTful API -- also referred to as a RESTful web service -- is based on representational state transfer (REST) technology, an architectural style and approach to communications often used in web services development. REST technology is generally preferred to the more robust Simple Object Access Protocol (SOAP) technology because REST leverages less bandwidth, making it more suitable for internet usage. An API for a website is code that allows two software programs to communicate with each another. The API spells out the proper way for a developer to write a program requesting services from an operating system or other application.

This technology is the best for the modern web. If you pay closer attention to your daily-visited websites, almost all of them work in this way. To try it, I recommend you to try to build a basic blog. [This tutorial](https://medium.com/@adigunhammedolalekan/build-and-deploy-a-secure-rest-api-with-go-postgresql-jwt-and-gorm-6fadf3da505b) is great for quick paced start.

# Continuous code deployment with AWS

One of the most important parts of successful project is a great beginning and it starts with picking right tools for the right job. This article should help you to understand what kind of tools you need to kickstart your project and of course how to implement them.

## AWS
---

[AWS](https://aws.amazon.com) (Amazon Web Services) are one of the best cloud computing services in the market. It is not that hard to launch a virtual machine and run your code in it. All you have to do is:

1) [Sign up to AWS](https://portal.aws.amazon.com/billing/signup#/start).
2) Launch a virtual machine. I would suggest to pick Ubuntu Server 18.04 LTS.
3) After reviewing your selection, you will be asked to create a new key pair. Do it and save the key somewhere safe because you will need it.
4) Run ssh to your new personal virtual machine:
```
ssh -i ~/{key_location}/{key_filename}.pem ubuntu@{Public DNS (IPv4)}
```

## Meet the Docker 🐋!
---
Docker is a magical program that performs operating-system-level virtualization, also known as "containerization". It keeps your development enviroment clean and makes code deployment easy. But before the fun begins, you have to install it:

1) Update the apt package index:
```
$ sudo apt-get update
```
2) Install packages to allow apt to use a repository over HTTPS:
```
$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
```
3) Add Docker’s official GPG key:
```
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
4) Verify that you now have the key with the fingerprint 9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88, by searching for the last 8 characters of the fingerprint:
```
$ sudo apt-key fingerprint 0EBFCD88
```
5) Use the following command to set up the stable repository:
```
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```
6) Update the apt package index:
```
$ sudo apt-get update
```
7) Install the latest version of Docker CE:
```
$ sudo apt-get install docker-ce
```

Next you will need to install [docker-compose](https://docs.docker.com/compose/overview/):

1) Run this command to download the latest version of Docker Compose:
```
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
2) Apply executable permissions to the binary:
```
$ sudo chmod +x /usr/local/bin/docker-compose
```

Only few steps left, try to keep up:

1) Create the docker group:
```
$ sudo groupadd docker
```
2) Add your user to the docker group:
```
$ sudo usermod -aG docker $USER
```
3) Open permission for docker socket
```
$ sudo chmod 777 /var/run/docker.sock
```

## Hello, this is Jenkins 🍸
---

Jenkis is the leading open source automation server, it provides hundreds of plugins to support building, deploying and automating any project. TLDR it saves your precious time.

1) Install it:
```
wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
```
2) Upgrade it:
```
sudo apt-get update
sudo apt-get install jenkins
```
3) You will be asked to enter the password. You can see it by opening file with vi:
```
$ vi /var/jenkins_home/secrets/initialAdminPassword
```

Now you have to open port 8080 of your AWS instance. You have to navigate to Security Group of your instance and add custom TCP rule:
![tcp](https://i.stack.imgur.com/qQZ5e.png) 

## Putting it all together...
---

After you have everything installed, you can try to set up Github integration.

1) In Jenkins go to Manage Jenkins -> Manage Plugin
![first step](https://valuebound.com/sites/default/files/inline-images/Image_3.png)
2) Search Github Plugin in the Available tab then click on Download now and install after the restart.
![2](https://1554227851.rsc.cdn77.org/sites/default/files/inline-images/image%203_0.jpg)
3) To Create a new task for Jenkins, click on “New Item” then enter an item name that is suitable for your project and select Freestyle project. Now click Ok. 
![3](https://1554227851.rsc.cdn77.org/sites/default/files/inline-images/image%204.jpg)
4) Select the GitHub project checkbox and set the Project URL to point to your GitHub Repository.
![4](https://1554227851.rsc.cdn77.org/sites/default/files/inline-images/image%205.jpg)
5) Under Source Code Management tab, select Git and then set the Repository URL to point to your GitHub Repository.
![5](https://valuebound.com/sites/default/files/inline-images/Image_7_0.png)
6) Now Under Build Triggers tab, select the “Build when a change is pushed to GitHub” checkbox.
![6](https://1554227851.rsc.cdn77.org/sites/default/files/inline-images/image%207.jpg)
7) At the end, execute Shell. When the configuration is done, click on save button.
![7](https://valuebound.com/sites/default/files/inline-images/Image_9.png)
8) Go to your Github repository settings and set up a webhook for Jenkins. The adress should be: {your DNS}:8080/github-webhook
![8](https://valuebound.com/sites/default/files/inline-images/Image_11_1.png)

## Node.js example

This example will show how you can easily configure containers for your project. The containers will run MongoDB and Node.js.

1) In src directory create Dockerfile
```
FROM node:latest
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
COPY package.json /usr/src/app/
RUN npm install
COPY . /usr/src/app
EXPOSE 3000
CMD [ “npm”, “start” ]
```

2) And in project directory create docker-compose.yml file
```
version: "2"
services:
  app:
    container_name: app
    restart: always
    build: .
    ports:
      - "3000:3000"
    links:
      - mongo
  mongo:
    container_name: mongo
    image: mongo
    volumes:
      - ./data:/data/db
    ports:
      - "27017:27017"
```

After pushing your code to Github repository, run shell or configure Jenkins shell to build and run your containers:
```
$ docker-compose up -d --build
```


<img src="https://i.imgur.com/zCL5SQV.jpg">

# React.js in a nutshell

React.js is a component based JavaScript framework that offers you quite an amazing experience in writing front-end code. What does component based actually mean? It means that a page will be born from many different components that will create a well-built page. But why do I need these magical components? The answer is simple – speed and extra functionality. Page loading speed and resources boost is visible while using React.js and it is because of the main treasure that this framework gives us – when a component reloaded, used or its state is changed ([More about states](https://reactjs.org/docs/state-and-lifecycle.html)), React does not reload the page – it only reload that certain component or component tree. This does dramatically improve overall page performance and saves a lot of internet usage. Extra functionality is mentioned before – component states. Components in React.js are classes that have practically the same type of functionality as usual different programming languages would have – scoped functions, variables and, in this case, local data storage for itself called state. It is now even hard to say that React.js is very promising, because even know it amazes with what it has to offer, so the moral would be that nowadays it’s a must to get familiar with this framework if you want to become a better front-end developer.

# Components that hide in our page

Our project consists of few pages and even more components. When you first open up our website the index page is our create-a-plan component. This component can be divided into smaller components as navigation bar, containers and buttons that shows us more component-based modals like BMI (Body mass index calculator). Below I will show you how does our navigation bar component code looks like.

```
import React from 'react';
import { BrowserRouter as Router, Link } from 'react-router-dom';
import './Navbar.css';
import logo from '../img/logo.png';

class Navbar extends React.Component {
  constructor(props) {
    super(props);
    this.state = { userLoggedIn:false };
  }

  render() {
    return (
        <nav id="sidebar">
          <div className="sidebar-header">
            <img alt="Nutri logo" src={logo} className="navLogo" />
          </div>
          <ul className="list-unstyled components">
            <li>
              <Link to="/">PAGRINDINIS</Link>
            </li>
            <li>
              <Link to="/recipes">RECEPTAI</Link>
            </li>
            <li>
              <Link to="/about">APIE NUTRI</Link>
            </li>
          </ul>
        </nav>
    );
  }
}

export default Navbar;

```

Let me explain a bit what is written here. So the first thing is we are importing React and Router libraries to our component, because if we don't - we would not be able to use any React or Routing functions inside this scope, including creating a properly working component for later use. Routing is something similar to navigating through pages with help of links in normal HTML, but it gives us more functionality and speed to burst around our components. Later in this code we include our navigation style sheet and one image file. Then a class is defined. That is where our component is born. Inside this class we have an unused state, that was supposed to be included in later updates, but for now we shall leave it like this. To explain state in simple words - we have a mark if user is logged in and it is set to false by default. Our component can easily change this by adding some other sign-up or login components that will manipulate this state and set it to true whenever a user will be authenticated. The render method create the visible part of this component in our page. Everything inside the return braces will be rendered in the DOM. If you have any experience with HTML, the code might be recognized as it is similar. But don't trick yourselves because there are things that differ from our ancient HTML language. As you can see, the first "div" inside the "nav" tag has a class named "sidebar-header". But take a look how this we define a class in React - we use "className" instead of simple "class". Later we include a logo image inside a self-closing tag "img". The path to our image is defined with curly braces like this "{logo}". The word "logo" inside the curly braces is actually the name of our image import we have on top of this code. Then we have a simple "ul" list that brings us the navigation itself. Using the Router library, we are offered to include <Link> components that help us navigate through our component-based pages. In this case, we have three different pages. And in the end, we have to export this component, that later can be used when imported in other components or files.
## Calories calculator
One of our project's components is calories calculator. It's purpose is to count calories that user needs to consume to stay the same size per day. This calories number is calculating by multiplying BMR (Basal metabolic rate)  which is the rate of energy expenditure per unit time at rest and user's physical activity.

To change states of data, that is needed to calories calculator, we use functions:
```
heightChange(e) {
this.setState({ height: e.target.value });
e.preventDefault();
}

weightChange(e) {
this.setState({ weight: e.target.value });
e.preventDefault();
}

ageChange(e) {
this.setState({ age: e.target.value });
e.preventDefault();
}

genderChange(e) {
this.setState({ gender: e.target.value });
}

activeChange(e) {
this.setState({ active: e.target.value });
e.preventDefault();
}
```

**Revised Harris-Benedict Equation** is used to calculate BMR.
For men: BMR = 13.397xWeight + 4.799xHeight - 5.677xAge + 88.362
For women: BMR = 9.247xWeight + 3.098xHeight - 4.330xAge + 447.593

After that BMR is multiplied by number, that indicates users physical activity.
```
caloriesCalculator() {

const maleBMR = (13.397 * this.state.weight) + (4.799 * this.state.height) - (5.677 * this.state.age) + 88.362;

const femaleBMR = (9.247 * this.state.weight) + (3.098 * this.state.height) - (4.330 * this.state.age) + 447.593;

let calories;

if (this.state.gender === 'male') {
if (this.state.active === 'passive') {
calories = maleBMR * 1.2;
this.setState({ calories: Math.round(calories) });
}
else if (this.state.active === 'mild') {
calories = maleBMR * 1.375;
this.setState({ calories: Math.round(calories) });
}
else if (this.state.active === 'moderate') {
calories = maleBMR * 1.55;
this.setState({ calories: Math.round(calories) });
}
else if (this.state.active === 'heavy') {
calories = maleBMR * 1.7;
this.setState({ calories: Math.round(calories) });
}
else if (this.state.active === 'extreme') {
calories = maleBMR * 1.9;
this.setState({ calories: Math.round(calories) });
}
}
else if (this.state.gender === 'female') {
if (this.state.active === 'passive') 
calories = femaleBMR * 1.2;
this.setState({ calories: Math.round(calories) });
}
else if (this.state.active === 'mild') {
calories = femaleBMR * 1.375;
this.setState({ calories: Math.round(calories) });
}
else if (this.state.active === 'moderate') {
calories = femaleBMR * 1.55;
this.setState({ calories: Math.round(calories) });
}
else if (this.state.active === 'heavy') {
calories = femaleBMR * 1.7;
this.setState({ calories: Math.round(calories) });
}
else if (this.state.active === 'extreme') {
calories = femaleBMR * 1.9;
this.setState({ calories: Math.round(calories) });
}
}
return calories;
}
```
Finally, to calculate everything and show it to user is used submit function:
```
submit(e) {
e.preventDefault();
const cals = Math.round(this.caloriesCalculator());
this.props.handler({
caloriesCount: cals
});
}
```
# How to use Nutri
1) Open home page.
<img src="https://i.imgur.com/NZOpbDI.png">
2) In the right side of the page press the button called "Kalorijų skaičiuoklė".
3) When modal window shows up, enter your height, weight and age and also choose your gender and physical activity. Then press button "Skaičiuoti" and it will count how much calories you need to consume to stay the same size per day.
<img src="https://i.imgur.com/zQSk4NL.png">
4) Close modal window and in slider "Dienos" choose, how much days do you want your menu to last.
5) After that, in the next slider "Valgymų kartai" choose, how much times in a day you want to eat. Whenever you change this slider, the menu regenerates on every slider or input change.
<img src="https://i.imgur.com/VO6rVRS.png">
6) Bellow all sliders, in an input named "Produktai, kurių neįtraukti į maisto racioną" you can write products, that you don't want to have in your meals. In example, this input lets you prevent from getting any allergic products in your meal plan. On input, a dropdown list will show up, and you can select only those products, that are stored in our database. 
<img src="https://i.imgur.com/JNPqGkI.png">
<img src="https://i.imgur.com/sx2c8d5.png">
7) In middle of the screen you can see generated meals in each day. Bellow the meal's name, there is time that is needed to prepare this meal.
8) If you want to see the recipe, or products that meal requires, you can open meal's modal window by clicking info icon on the selected meal, which is on it's left side. Also in that window you can see calories, proteins and carbohydrates that your chosen meal has.
<img src="https://i.imgur.com/Gn3i6Zd.png">
9) If you don't like some of meals, you can delete them by pressing trash bin icon on the selected meal, which is on it's right side.
10) If you want to regenerate some of meals, you can do it, by clicking on refresh icon on the selected meal, which is on it's right side. If you want to regenerate all day's meals, you can do it, by clicking refresh icon on the top of all meals, next to button "Produktų krepšelis".
11) When you have your meals checked, you can see products, that you will need,  and their quantities and prices by clicking on button "Produktų krepšelis".
12) Before the products are generated in a shopping cart format table, there is an amazing preloader to entertain you until the moment of greatness appears.
<img src="https://i.imgur.com/HnPAuBx.png">
12) Download your product list, and start preparing your meals.

# Install this package in your local machine

To install and be able to use our project for well-being purposes you need to follow these few simple steps to get going.

1) Install Node.js and Git bash command line interfaces.
2) Open terminal with git bash command prompt and in navigate into your preffered folder that you want to install this package in.
3) Run these commands: 
```
git clone https://github.com/VUNutri/APP.git
cd APP
npm install
```
4) Now you have set up our package and installed all dependecy packages, that are needed in order to be able to work with this project. Now to run it, you need to enter this simple command.
```
npm start
```
5) Thats it! You have now successfully began to emulate this project and your browser should open this page after this action.
