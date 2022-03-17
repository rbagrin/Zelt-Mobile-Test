# Zelt Mobile Test
## Instructions
Congratulations, you made it to the next step at Zelt's recruiting process! At this stage, we need to check your techinical skills by asking you to do what you like the most: writing code. In this technical challenge we would like to see your best work. The most important aspects that we're going to judge is your capacity to produce high quality code that is well organised, readable, testable and that follows the best practices in the software engineering industry. We'd like you to create a private repository (you can fork this repo or you can clone it and then use the code for your repo) and invite us (github usernames: **rbagrin**, **elgutierrez**) to have access to it. We expect you to collaborate with us the same way that you'd do in a daily basis when working at Zelt, meaning:

* Create (one or multiple, at your discretion) pull requests with your changes.
* Write clear commit messages and keep your commit history clean.
* We would like to see some tests (ideally using Jest).
* It would be nice to give some attention to the UI/UX aspect.

## Brief
1. Create a Mobile app where you can see the list of superheroes that you can retrieve by calling the backend API we have provided (more details below).
2. The home page should display the list of superheroes.
3. You should be able also to add superheroes.
4. All the pages that you are creating should be protected login protected (except the login page) meaning you can access those only if you are logged in.
5. (Optional) The list of superheroes should provide links to each of the superhero's page.
6. (Optional) Delete superhero action.

## Backend description
### Entities
**Hero**
* id - number - id of record
* name - string - name of the superhero
* shortDescription - string - a 1-2 sentences short description of the superhero
* description - string - a longer and more detailed description of the superhero
* power - string - a list of powers of the superhero separated by commas

### Endpoints
**POST /login** 
* sets the JWT token in a cookie (token='<JWT_token>') and returns "Success" if the login is successfull. Throws a 401 error otherwise.
* body data - { name: string; password: string; }
* you can use the following credentials to execute a successfull authentication: { name: "Test", password: "1234" }

**POST /logout**
* removes the JWT token saved in the cookie and returns "Success" if the logout is successfull.


**GET /heroes**
* returns an array of superheroes
* can be used only if authenticated

**GET /heroes/:id**
* returns the details of a superhero
* can be used only if authenticated

**POST /heroes**
* creates a new superheroes
* body data - { name: string; shortDescription: string; description: string; power: string; }
* can be used only if authenticated

**DELETE /heroes/:id**
* deletes a superhero by id
* can be used only if authenticated

## Requirements
- [ ] use any Mobile Framework you are comfortable with
- [ ] pages required: /login, /superheroes (the list of heroes), (optional /superheroes/:id - superhero details page)
- [ ] home page should list all the superheroes (can use a list, a table, cards or whatever you think it would look nice and would do the job)
- [ ] on the hompage you should be able to add a new superhero
- [ ] if not logged in - only the login page is available

## Tips and advices
* Feel free to design the pages you are creating as you wish. We will also appreciate the creativity, not only the code.
* Feel free to add improvements/features (not a requirement).
* Write clean code and try not having all the code of a page in the same file.

## Backend set up
You will need Node JS (^14.0) installed to be able to run the server. 
From one terminal go inside the **/backend** folder and:
* run **npm install**
* run **npm run start:dev**
* the api is now accessible on the **port 8000**

###### * the api accepts request only from **http://localhost:3000** (if you want to change the port the server is expecting requests from, you'll have to search for *origin: 'http://localhost:3000',* in /backend/src/main.ts and update the port you are sending the requests from)

###### You also should let us know how we can run/test your mobile app, depending on the framework you are using.

## Good luck!
