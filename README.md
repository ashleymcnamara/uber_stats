**UberStats** is a statistics app where users can log in with their Uber accounts and are provided with insights into their ride history.

UberStats was created by [Ashley McNamara](<ashleymcnamara1@gmail.com). You can connect with Ashley on [LinkedIn](https://www.linkedin.com/in/ashleymcnamara) and [Twitter](https://twitter.com/ashleymcnamara)


# Table of Contents
* [Technologies](#technologies)
* [Features](#features)
* [Installation](#install)
* [Deployment](#deployment)
* [Version 2.0](#future)
* [Author](#author)

## <a name="technologies"></a>Technologies

**UberStats** is built on a Flask server (written in Python) and uses an encoding technique called base64 the application seamlessly integrates with Uber and adopts a modernized UI.

Tech Stack:
* Frontend: [Jinja2](http://jinja.pocoo.org/docs/dev/), [HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5), [CSS3](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS3)
* Backend: [Python](https://www.python.org/), [Flask](http://flask.pocoo.org/)
* base64: [base64](https://en.wikipedia.org/wiki/Base64)
* API: [Uber](https://developer.uber.com/)

(Dependencies are listed in [requirements.txt](requirements.txt).)

## <a name="features"></a>Features

####Login with Uber

User login is handled through Uber's OAuth 2.0, following the client-side authorization flow. 

###_What does UberStats OAuth flow look like?_

For a user to access UberStats content and request in-app Uber services, the app needs authorization from Uber and redirects the user to Uber's Authorization server, where the user is asked to authenticate (if not already logged in) and then authorize the requested permissions. After successfully being granted access, the app is redirected from Uber to the redirect uri address, including an access token that can be used directly by the app to request information or perform operations on behalf of the user. 

The access token is then encrypted and stored on the Flask session, and the user's subsequent login will not prompt for the authorization dialog if the user is logged in and has previously approved the same permissions. For more, please see the [Uber API documentation](https://developer.uber.com/docs/authentication).

####User Profile and Avatar

Upon a user's successful login through Uber, the app accesses the user's Uber profile and greets the user with the user's name and Uber profile picture on top of the results page. Next, you'll see the number of cities where Uber was used, number of rides taken and in different product types, miles travelled in Uber, total time spent waiting for an Uber, and total time spent in an Uber.

If you want to get a copy of this project up and running on your local machine for development and testing purposes, here are the steps

####Set up

Clone this repository.
```
$ git clone https://github.com/ashleymcnamara/uber_stats
```
Create a virtual environment for the project.
```
$ virtualenv env
```
Activate the virtual environment.
```
$ source env/bin/activate
```
Install dependencies.
```
$ pip install -r requirements.txt
```
To enable the Uber functionality, you should set up your own developer accounts and have your own sets of API keys and tokens. 

## <a name="deployment"></a>Deployment

Deployment details to come!

## <a name="future"></a>Version 1.0

Future features to come:

- [ ] Profile Picture
- [ ] Leader board
- [ ] More testing

## <a name="author"></a>Author

**Ashley McNamara** (Github: [ashleymcnamara](https://github.com/ashleymcnamara)) is a Developer Advocate and lives in Austin Texas. 

## <a name="license"></a>License

This project is licensed under the MIT License. See the [LICENSE.txt](LICENSE.txt) file for details.
