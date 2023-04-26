# My Friend Morgan
# /**exercise**

API endpoints for /exercise<br>

## **GET /exercise/outside-elc-url**
Constructs the survey url string for survey outside of elc and returns it

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session’s ID

## **POST /exercise/start-survey**
Constructs the survey url string for in elc and sends it through the show-survey server side event, along with first name, last name, and session name

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session’s ID

## **POST /exercise/start-case-scenario**
Generate the case scenarios for each room. Constructs the case scenario response url string and sends it through the show-case-scenario server side event, along with first name, last name, and session name

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session’s ID

## **POST /exercise/start-group-response**
Sends first name, last name, and session name through show-group-response server side event.

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session’s ID

## **GET /exercise/get-individual-results**
Compile individual results for that session and returns them.

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session’s ID

## **GET /exercise/get-group-results**
Compile room results for that session and returns them.

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session’s ID

## **GET /exercise/events**
### Server side events: 
- show-survey 
- show-case-scenario
- show-group-response
