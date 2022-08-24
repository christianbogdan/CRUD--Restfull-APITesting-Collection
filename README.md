# Restfull-APITesting-Collection
My first API Testing Project in POSTMAN / All operations have been carried out CRUD ( Create, Read, Update, Delete )
## About the project 
The project was carried out with the help of those from https://restful-booker.herokuapp.com who also provided me with the necessary documentation for API testing.
## Create Environments 
We have achieved 3 environments to make our work easier. 

1. "env" - It was created to contain our endpoint https://restful-booker.herokuapp.com 
2. "token" - It was created to contain the authorization token 
3. "bookingid" - It was created to contain the ID of the desired book 

<img width="600" alt="Screenshot 2022-08-24 at 16 43 05" src="https://user-images.githubusercontent.com/34375010/186434913-b5b58503-d493-40f1-922e-125f70005b94.png">

## Use of Snippets 
We used different snippets to automate the testing process.

## CRUD Operations

1. GET Ping Server

:triangular_flag_on_post: Snippets 

``` 
pm.test("Created", function () {
    pm.expect(pm.response.text()).to.include("Created");
}); 

``` 
This snippet was created to test whether it comes as a "created" response.

<img width="600" alt="Screenshot 2022-08-24 at 17 04 34" src="https://user-images.githubusercontent.com/34375010/186439217-f36dd0c6-1158-4394-908d-fade55428411.png">

2. POST Auth 

:triangular_flag_on_post: Snippets  

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain token", function () {
    pm.expect(pm.response.text()).to.include("token");
});
var jsonData = JSON.parse(responseBody);
postman.setEnvironmentVariable("token", jsonData.token);
pm.globals.set("token", jsonData.token )
``` 
This snippet was created to check status 200 if the answer received contains the word "token".

<img width="600" alt="Screenshot 2022-08-24 at 17 12 53" src="https://user-images.githubusercontent.com/34375010/186441244-db9fa236-b06b-44ba-a378-24266d877cf3.png">

3. Auth without Username&Password 

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 17 00" src="https://user-images.githubusercontent.com/34375010/186442152-df6cf4b8-a93d-4741-b121-a8d86cd72054.png">

<img width="600" alt="Screenshot 2022-08-24 at 17 18 26" src="https://user-images.githubusercontent.com/34375010/186442462-85c28c41-b595-483b-8b82-80eb3c325b86.png">

4. Auth without Password 

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 22 21" src="https://user-images.githubusercontent.com/34375010/186443318-0df51198-fc8c-4f73-a197-98eca3e8c655.png">
<img width="600" alt="Screenshot 2022-08-24 at 17 23 04" src="https://user-images.githubusercontent.com/34375010/186443502-417cdb38-cec6-4bf7-87a4-f0298faaa747.png">


5. Auth without Username 

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 22 21" src="https://user-images.githubusercontent.com/34375010/186443318-0df51198-fc8c-4f73-a197-98eca3e8c655.png">

6. Auth with blank password

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 26 26" src="https://user-images.githubusercontent.com/34375010/186444217-1f811dcd-2144-4730-b5ac-e45c18da2316.png">

7. Auth with blank username

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 27 49" src="https://user-images.githubusercontent.com/34375010/186444554-4cc47352-88c9-41bd-ba8e-72b6472d117a.png">

8. Auth with wrong Username&Password

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 29 08" src="https://user-images.githubusercontent.com/34375010/186444955-b9f3bcc7-1fd4-484f-8740-d4b2e57140ef.png">


9. Auth with wrong Username

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials".

<img width="600" alt="Screenshot 2022-08-24 at 17 36 27" src="https://user-images.githubusercontent.com/34375010/186446677-71bda02d-d84a-48f9-9b2d-1c48e4380b6c.png">

10. Auth with wrong Password

:triangular_flag_on_post: Snippets 

``` 
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response body contain Bad credentials", function () {
    pm.expect(pm.response.text()).to.include("Bad credentials");
});

```
This snippet was created to check status 200 if the answer received contains "Bad credentials". 

<img width="600" alt="Screenshot 2022-08-24 at 17 33 51" src="https://user-images.githubusercontent.com/34375010/186446072-58d9ac26-e422-4baf-88f8-63b1c1b3d92f.png">

11. Create new booking 

:triangular_flag_on_post: Snippets 

 ```
 pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Body contain bookingid", function () {
    pm.expect(pm.response.text()).to.include("bookingid");
});

pm.test("Body contain firstname", function () {
    pm.expect(pm.response.text()).to.include("firstname");
});

pm.test("Body contain Cristian", function () {
    pm.expect(pm.response.text()).to.include("Cristian");
});

pm.test("Body contain lastname", function () {
    pm.expect(pm.response.text()).to.include("lastname");
});

pm.test("Body contain Cristian", function () {
    pm.expect(pm.response.text()).to.include("Cristian");
});

pm.test("Body contain totalprice", function () {
    pm.expect(pm.response.text()).to.include("totalprice");
});

pm.test("Body contain 150", function () {
    pm.expect(pm.response.text()).to.include("150");
});

pm.test("Body contain depositpaid", function () {
    pm.expect(pm.response.text()).to.include("depositpaid");
});

pm.test("Body contain false", function () {
    pm.expect(pm.response.text()).to.include("false");
});

pm.test("Body contain bookingdates", function () {
    pm.expect(pm.response.text()).to.include("bookingdates");
});

pm.test("Body contain checkin", function () {
    pm.expect(pm.response.text()).to.include("checkin");
});

pm.test("Body contain checkout", function () {
    pm.expect(pm.response.text()).to.include("checkout");
});

pm.test("Body contain additionalneeds", function () {
    pm.expect(pm.response.text()).to.include("additionalneeds");
});

var jsonData = JSON.parse(responseBody);
pm.globals.set("bookingid", jsonData.bookingid)

 ```

This snippet was created to check the status of 200 if the answer received contains the following: Bookingid, firstname, Cristian, lastname, Cristian, totalprice, 150, depositpaid, false, bookingdates, checkin, checkout, addtionalneeds. 

<img width="600" alt="Screenshot 2022-08-24 at 17 43 26" src="https://user-images.githubusercontent.com/34375010/186448381-5e604404-98a8-409f-a7f8-0c0036706ab7.png"> 
   



