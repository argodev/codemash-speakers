#speakersdata

Available Methods:

* [`GET api/speakersdata`](#get-apispeakersdata)
* [`GET api/speakersdata/{id}`](#get-apispeakersdataid)

Examples:
* Simple html example: [../examples/speakers.html](../examples/speakers.html)

##GET api/speakersdata

###Request Information
__URI Parameters__
* None

__Body Parameters__
* None

###Response Information
####Resource Description
Collection of `PublicSpeakerDataModel`

| Name        | Description                                  | Type   |
|-------------|----------------------------------------------|--------|
| Id          | Unique ID for this speaker                   | string |
| FirstName   | Speaker's first name                         | string | 
| LastName    | Speaker's last name                          | string |
| Biography   | Speaker-provided biography. May be long      | string |
| GravatarUrl | URL to speaker image based on provided image | string |

####Response Formats

__application/json, text/json__
```
[
    {
        "Id": "a02a0671-98a9-4365-a7b5-b963c6b4b046",
        "FirstName": "Sample String 1",
        "LastName": "Sample String 2",
        "Biography": "A (potentially) really long Sample String",
        "GravatarUrl": "//www.gravatar.com/avatar/06f6516772eca8763479753e2746e328"
    },
    {
        "Id": "0d77e7b9-8315-4197-a135-6091933cbda0",
        "FirstName": "Sample String 1",
        "LastName": "Sample String 2",
        "Biography": "A (potentially) really long Sample String",
        "GravatarUrl": "//www.gravatar.com/avatar/25ddbfa83fef9e5f8f1e15c73d1de9e1"
    }
]
```

__application/xml, text/xml__
```
<ArrayOfPublicSpeakerDataModel>
    <PublicSpeakerDataModel>
        <Id>a02a0671-98a9-4365-a7b5-b963c6b4b046</Id>
        <FirstName>Sample String 1</FirstName>
        <LastName>Sample String 2</LastName>
        <Biography>A (potentially) really long Sample String</Biography>
        <GravatarUrl>
            //www.gravatar.com/avatar/06f6516772eca8763479753e2746e328
        </GravatarUrl>
    </PublicSpeakerDataModel>
    <PublicSpeakerDataModel>
        <Id>0d77e7b9-8315-4197-a135-6091933cbda0</Id>
        <FirstName>Sample String 1</FirstName>
        <LastName>Sample String 2</LastName>
        <Biography>A (potentially) really long Sample String</Biography>
        <GravatarUrl>
            //www.gravatar.com/avatar/25ddbfa83fef9e5f8f1e15c73d1de9e1
        </GravatarUrl>
    </PublicSpeakerDataModel>
</ArrayOfPublicSpeakerDataModel>
```



##GET api/speakersdata/{id}

###Request Information
__URI Parameters__

| Name        | Description                | Type   | Additional Information |
|-------------|----------------------------|--------|------------------------|
| Id          | Unique ID for the speaker  | string | Required               |

__Body Parameters__
* None

###Response Information
####Resource Description
Instance of `PublicSpeakerDataModel`

| Name        | Description                                  | Type   |
|-------------|----------------------------------------------|--------|
| Id          | Unique ID for this speaker                   | string |
| FirstName   | Speaker's first name                         | string | 
| LastName    | Speaker's last name                          | string |
| Biography   | Speaker-provided biography. May be long      | string |
| GravatarUrl | URL to speaker image based on provided image | string |

####Response Formats

__application/json, text/json__
```
{
    "Id": "a02a0671-98a9-4365-a7b5-b963c6b4b046",
    "FirstName": "Sample String 1",
    "LastName": "Sample String 2",
    "Biography": "A (potentially) really long Sample String",
    "GravatarUrl": "//www.gravatar.com/avatar/06f6516772eca8763479753e2746e328"
}
```

__application/xml, text/xml__
```
<PublicSpeakerDataModel>
    <Id>a02a0671-98a9-4365-a7b5-b963c6b4b046</Id>
    <FirstName>Sample String 1</FirstName>
    <LastName>Sample String 2</LastName>
    <Biography>A (potentially) really long Sample String</Biography>
    <GravatarUrl>
        //www.gravatar.com/avatar/06f6516772eca8763479753e2746e328
    </GravatarUrl>
</PublicSpeakerDataModel>
```
