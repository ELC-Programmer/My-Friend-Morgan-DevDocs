# My Friend Morgan
# **/session**

API endpoints for /session<br>

## **GET /session/get-sessions**
Returns a list of all sessions belonging to a professor

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name

### Sample Response
```
[
    {
        "_id": "643d692a98d5e1de084917fc",
        "firstName": "Carol",
        "lastName": "Folt",
        "sessionId": "123",
        "surveyAtElc": true,
        "createdAt": 1681746218452,
        "building": "Fertitta Hall",
        "rooms": [
            "JFF Room A",
            "JFF Room B",
            "JFF Room C"
        ],
        "surveyDone": true
    },
]
```
## **POST /session/create**
Creates a session and stores it in the database

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session's ID
- surveyAtElc - Whether the surveyis being done at the ELC

## **POST /session/delete**
Deletes a session from the database

### Parameters
- firstName - Professor’s first name
- lastName - Professor’s last name
- sessionId - Session's ID

## **GET /session/available-rooms**
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