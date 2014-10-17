#sessionsdata

Available Methods:

* [`GET api/sessionsdata`](#get-apisessionsdata)
* [`GET api/sessionsdata/{id}`](#get-apisessionsdataid)

Examples:
* Simple html example: [../examples/sessions.html](../examples/sessions.html)

##GET api/sessionsdata

###Request Information
__URI Parameters__
* None

__Body Parameters__
* None

###Response Information
####Resource Description
Collection of `PublicSessionDataModel`

| Name        | Description                                  | Type   |
|-------------|----------------------------------------------|--------|
| Id          | Unique ID for this session                   | int    |
| Title       | Title of the session                         | string |
| Abstract    | Abstract for the session. May be long.       | string |
| SessionType | Type of session. Fixed set of strings.       | string |
| Tags        | 0 or more tags describing the session        | collection of strings |
| Speakers    | 0 or more speakers for this session | collection of PublicSpeakerThinDataModel |


`PublicSpeakerThinDataModel`

| Name        | Description                                  | Type   |
|-------------|----------------------------------------------|--------|
| Id          | Unique ID for this speaker                   | string |
| FirstName   | Speaker's first name                         | string | 
| LastName    | Speaker's last name                          | string |
| Biography   | Speaker-provided biography. May be long      | string |
| GravatarUrl | URL to speaker image based on provided email | string |

####Response Formats

__application/json, text/json__
```
[
    {
        "Id": 1,
        "Title": "Sample String 1",
        "Abstract": "Sample long string",
        "SessionType": "Regular Session",
        "Tags": [
            "Mobile"
        ],
        "Speakers": [
            {
                "Id": "fce6393b-0186-431f-be91-85ebd2ee453f",
                "FirstName": "Sample String 3",
                "LastName": "Wedinger",
                "GravatarUrl": "//www.gravatar.com/avatar/06f6516772eca8763479753e2746e328"
            }
        ]
    },
    {
        "Id": 2,
        "Title": "Sample String 1",
        "Abstract": "Sample long string",
        "SessionType": "Pre-Compiler",
        "Tags": [
            "JavaScript",
            "Ruby/Rails",
            ".NET",
            "Testing"
        ],
        "Speakers": [
            {
                "Id": "3c57b6bb-9753-438f-9610-6fe49d0d645b",
                "FirstName": "Sample String 3",
                "LastName": "Sample String 4",
                "GravatarUrl": "//www.gravatar.com/avatar/25ddbfa83fef9e5f8f1e15c73d1de9e1"
            },
            {
                "Id": "fce6393b-0186-431f-be91-85ebd2ee453f",
                "FirstName": "Sample String 3",
                "LastName": "Sample String 4",
                "GravatarUrl": "//www.gravatar.com/avatar/06f6516772eca8763479753e2746e328"
            }
        ]
    }
]
```

__application/xml, text/xml__
```
<ArrayOfPublicSessionDataModel xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://schemas.datacontract.org/2004/07/CodeMash.Speakers.Web.Models">
    <PublicSessionDataModel>
        <Id>1</Id>
        <Title>Sample String 1</Title>
        <Abstract>Sample long string</Abstract>
        <SessionType>Regular Session</SessionType>
        <Speakers>
            <PublicSpeakerThinDataModel>
                <Id>fce6393b-0186-431f-be91-85ebd2ee453f</Id>
                <FirstName>Sample String 3</FirstName>
                <LastName>Sample String 4</LastName>
                <GravatarUrl>//www.gravatar.com/avatar/06f6516772eca8763479753e2746e328</GravatarUrl>
            </PublicSpeakerThinDataModel>
        </Speakers>
        <Tags xmlns:d3p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <d3p1:string>Mobile</d3p1:string>
        </Tags>
    </PublicSessionDataModel>
    <PublicSessionDataModel>
        <Id>2</Id>
        <Title>Sample String 1</Title>
        <Abstract>Sample long string</Abstract>
        <SessionType>Pre-Compiler</SessionType>
        <Speakers>
            <PublicSpeakerThinDataModel>
                <Id>3c57b6bb-9753-438f-9610-6fe49d0d645b</Id>
                <FirstName>Sample String 3</FirstName>
                <LastName>Sample String 4</LastName>
                <GravatarUrl>//www.gravatar.com/avatar/25ddbfa83fef9e5f8f1e15c73d1de9e1</GravatarUrl>
            </PublicSpeakerThinDataModel>
            <PublicSpeakerThinDataModel>
                <Id>fce6393b-0186-431f-be91-85ebd2ee453f</Id>
                <FirstName>Sample String 3</FirstName>
                <LastName>Sample String 4</LastName>
                <GravatarUrl>//www.gravatar.com/avatar/06f6516772eca8763479753e2746e328</GravatarUrl>
            </PublicSpeakerThinDataModel>
        </Speakers>
        <Tags xmlns:d3p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
            <d3p1:string>JavaScript</d3p1:string>
            <d3p1:string>Ruby/Rails</d3p1:string>
            <d3p1:string>.NET</d3p1:string>
            <d3p1:string>Testing</d3p1:string>
        </Tags>
    </PublicSessionDataModel>
</ArrayOfPublicSessionDataModel>
```



##GET api/sessionsdata/{id}

###Request Information
__URI Parameters__

| Name        | Description                | Type   | Additional Information |
|-------------|----------------------------|--------|------------------------|
| Id          | Unique ID for the session  | int    | Required               |

__Body Parameters__
* None

###Response Information
####Resource Description
Instance of `PublicSessionDataModel`

| Name        | Description                                  | Type   |
|-------------|----------------------------------------------|--------|
| Id          | Unique ID for this session                   | int    |
| Title       | Title of the session                         | string |
| Abstract    | Abstract for the session. May be long.       | string |
| SessionType | Type of session. Fixed set of strings.       | string |
| Tags        | 0 or more tags describing the session        | collection of strings |
| Speakers    | 0 or more speakers for this session | collection of PublicSpeakerThinDataModel |


`PublicSpeakerThinDataModel`

| Name        | Description                                  | Type   |
|-------------|----------------------------------------------|--------|
| Id          | Unique ID for this speaker                   | string |
| FirstName   | Speaker's first name                         | string | 
| LastName    | Speaker's last name                          | string |
| Biography   | Speaker-provided biography. May be long      | string |
| GravatarUrl | URL to speaker image based on provided email | string |

####Response Formats

__application/json, text/json__
```
{
    "Id": 1,
    "Title": "Sample String 1",
    "Abstract": "Sample long string",
    "SessionType": "Regular Session",
    "Tags": [
        "Mobile"
    ],
    "Speakers": [
        {
            "Id": "fce6393b-0186-431f-be91-85ebd2ee453f",
            "FirstName": "Sample String 3",
            "LastName": "Wedinger",
            "GravatarUrl": "//www.gravatar.com/avatar/06f6516772eca8763479753e2746e328"
        }
    ]
}
```

__application/xml, text/xml__
```
<PublicSessionDataModel>
    <Id>1</Id>
    <Title>Sample String 1</Title>
    <Abstract>Sample long string</Abstract>
    <SessionType>Regular Session</SessionType>
    <Speakers>
        <PublicSpeakerThinDataModel>
            <Id>fce6393b-0186-431f-be91-85ebd2ee453f</Id>
            <FirstName>Sample String 3</FirstName>
            <LastName>Sample String 4</LastName>
            <GravatarUrl>//www.gravatar.com/avatar/06f6516772eca8763479753e2746e328</GravatarUrl>
        </PublicSpeakerThinDataModel>
    </Speakers>
    <Tags xmlns:d3p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
        <d3p1:string>Mobile</d3p1:string>
    </Tags>
</PublicSessionDataModel>
```
