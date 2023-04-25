# My Friend Morgan
# **/submit**

API endpoints for /submit

## **POST /submit/survey-response**
Writes survey to the DB

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session’s ID

<mark>Check if below sample structure is correct</mark>  
### Sample Response
```
[
    {
        "_id": "643d692a98d5e1de084917fd",
        "firstName": "Carol",
        "lastName": "Folt",
        "sessionId": "123",
        "building": "Fertitta Hall",
        "room": "JFF Room A",
        "surveyData": {
            ???????
        }
    },
]
```
## **POST /submit/individual-response**
Writes individual case scenario response to the DB

### Parameters
- None

## **POST /submit/group-response**
Writes group case scenario response to the DB

### Parameters
- None

## **GET /submit/events**
Returns all existing rooms and their availability

### Parameters
- None

### Sample Response
```
[
    {
        "_id": "643d692a98d5e1de084917fc",
        "building": "Fertitta Hall",
        "rooms": [
            {
                "name": "JFF Room A",
                "currentSession": {
                    "firstName": "Carol",
                    "lastName": "Folt",
                    "sessionId": "123"
                }
            },
            {
                "name": "JFF Room B",
                "currentSession": null
            }
        ]
    },
    {
        "building": "Popovich Hall",
        "rooms": [
            {
                "name": "JKP Room 301A",
                "currentSession": null
            },
        ]
    },
    {
        "building": "Zoom",
        "rooms": []
    }
]
```
## **POST /session/start**
Adds rooms to the session

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session's ID
- building - Building Name
- rooms - Array of room names to add to the session

## **GET /session/download-results**
Downloads the exercise survey results and case scenario responses as tsv files in a zipped file, then deletes the session from the database

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session's ID