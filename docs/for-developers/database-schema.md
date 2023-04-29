# My Friend Morgan
# **Database Schema**


### [Setting up the **rooms** Collection](/rooms-collection-setup.md)

## Example Documents:

### **admin** Collection
```
{
    firstName: string,
    lastName: string,
    sessionIds: String<Array>
}
```

### **caseScenarios** Collection
```
{
    firstName: string,
    lastName: string,
    sessionId: string,
    room: string,
    studentUrl: string,
    caseScenario: string,
    behaviors: {
        lifetime: Array<String>
        pastime: Array<String>
    }
}
```

### **groupResponses** Collection
```
{
    first: string,
    last: string,
    sessionID: string,
    room: string,
    recommendation: string,
    reason: string,
    gender: string,
    genderReason: string
}
```

### **individualResponses** Collection
```
{
    first: string,
    last: string,
    sessionID: string,
    room: string,
    recommendation: string,
    reason: string,
    gender: string,
    genderReason: string
}
```
### **rooms** Collection
```
{
    building: string
    rooms: Array (
        {
            name: string,
            currentSession: {
                firstName: string,
                lastName: string,
                sessionId: string
            }
        }
    )
}
```

### **sessions** Collection
```
{
    firstName: string,
    lastName: string,
    sessionId: string,
    surveyAtElc: boolean,
    createdAt: number,
    building: string,
    rooms: Array<String>,
    surveyDone: boolean
}
```

### **surveyResponses** Collection
```
{
    first: string,
    last: string,
    sessionID: string,
    building: string,
    room: string,
    surveyData: {
        1: {
            lifetime: boolean,
            recently: boolean
        }
        .
        .
        .
        17: {
            lifetime: boolean,
            recently: boolean
        }
    }
}
```