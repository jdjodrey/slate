# Resources

## Team

Parameter | Description | Format
--------- | ----------- | ------
id | Unique identifier for a team | integer
label | Name of the team | string
athletePositions[] | Athlete position options for team | array
athletePositions[].label | Name of the position | string
athleteStatuses[] | Athlete status options for team | array
athleteStatuses[].label | Name of the athlete status | string
athleteStatuses[].labelPlural | Plural version of label | string
athleteStatuses[].isActiveStatus | Whether this status is considered "active" | boolean
userTypes[] | User type options for organization | array
userTypes[].label | Name of the user type | string

## User

Parameter | Description | Format
--------- | ----------- | ------
academicYear | The academic year of an athlete | string
active | Whether the user's account is active or not | boolean
athletePositions[] | The positions assigned to an athlete | array
athletePositions[].isStarter | Whether this athlete is a starter at this position | boolean
athletePositions[].label | Name of the position | string
athletePositions[].labelShort | Initials or short abbreviation for the position | string
athletePositions[].rank | The numerical rank of the athlete for this position | integer
athleteStatus | The status of an athlete | string
automobile | User's automobile information | object
automobile.make | | string
automobile.model | | string
automobile.plateNumber | | string
automobile.plateState | Two digit US state code (e.g. AL, NC, etc.) | string
automobile.year | Four digit year (e.g. 2015) | integer
custom | Contains all custom attributes applicable to this user. The "extra" URL parameters must include the value "custom" | object
dateOfBirth | User's birthdate | date
directReport | Direct report for this user | object
directReport.id | User id of the direct report | integer
directReport.name | Name of the direct report | integer
driversLicense | Drivers license information | object
driversLicense.expirationDate | When the drivers license expires | date
driversLicense.number | Drivers license number | string
driversLicense.state | License state. Two-digit US state code (e.g. AL, NC, etc.) | string
emailAddress | Primary email address of user | string
emailAddressAlternate | Alternate email address | string
facebookAccount | Facebook profile name (not full URL) | string
firstName | First name of the user | string
gender | Gender of the user (e.g. "Male" or "Female") | string
hasScholarship | Whether an athlete in on scholarship | boolean
id | Unique identifier value for a user | integer
jerseyNumber | Athlete jersey number | string
lastName | Last name of the user | string
major | Academic major for an athlete | string
metadata[] | Contains any enum options or custom attributes. The "extra" URL parameters must include the value "metadata" | array
metadata[].dataType | Data type of the attribute (e.g. string, boolean, numeric, list) | string
metadata[].enumOptions[] | Array of enum options for this attribute which must be sent when modifying this attribute | array
metadata[].isCustom | Whether this attribute was created by the client | boolean
metadata[].label | Descriptive name of attribute | string
metadata[].multiple | If attribute is of "array" data type, this indicates whether multiple values can be saved | boolean
metadata[].property | Associated property name returned in a normal resource representation | string
middleName | Middle name of user | string
nickname | Nickname of user | string
orgID | Unique identifier value of the user used by customer systems | string
phoneFax | Fax number of the user. For US, should be 10 digits. International numbers should start with "+" and the country code. | string
phoneHome | Home number of the user. For US, should be 10 digits. International numbers should start with "+" and the country code. |string
phoneMobile | Mobile number of the user. For US, should be 10 digits. International numbers should start with "+" and the country code. | string
phoneOffice | Office number of the user. For US, should be 10 digits. International numbers should start with "+" and the country code. | string
pictureImage | URL for user's profile picture | string
preferredName | Preferred name of the user (first name or nickname) | string
scholarshipAmount | Amount of scholarship if athlete has scholarship | string
startDate | Start date of the user | date
suffix | Suffix of the user's name (e.g. "Jr.", "III", etc.) | string
title | Title of the user (e.g. "Mr", "Ms", etc.) | string
twitterAccount | Twitter account of the user (not the full URL) | string
userTypes[] | Array of user types the user has on the team | array
userTypes[].label | Name of the user type | string
usesExternalAuthentication | Whether user authenticates using Single Sign-On (SSO) instead of Teamworks credentials. | boolean

## User Address

Parameter | Description | Format
--------- | ----------- | ------
city | City for address | string
country | Use the ISO alpha-2 letter code: [https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) | string
description | Description of the address (e.g. Home, Campus, etc) |  string
id | Unique identifier value for this address | integer
state | State or province for address | string
street | Street address | string
street2 | Additional street address | string
zip | Zip or postal code | string

## User Contact

Parameter | Description | Format
--------- | ----------- | ------
address | Address for the user’s contact (see [User Address](#user-address) resource above) | object
dateOfBirth | Birthdate of the contact | date
emailAddress | Email address of the contact | string
firstName | First name of the contact | string
id | Unique identifier value for this contact | integer
lastName | Last name of the contact | string
maritalStatus | Marital status of the contact. Has to be the label of a defined Relationship enum option. (defaults to "Unknown") | string
phoneHome | Home number of the user. For US, should be 10 digits. International numbers should start with "+" and the country code.| string
phoneMobile | Mobile number of the user. For US, should be 10 digits. International numbers should start with "+" and the country code. | string
phoneOffice | Office number of the user. For US, should be 10 digits. International numbers should start with "+" and the country code. | string
relationship | Relationship of the contact to the user. Has to be the label of a defined Relationship enum option (defaults to "Unknown") | string

## Event

Parameter | Description | Format
--------- | ----------- | ------
allDay | If the event spans all day or not | boolean
appointmentType | The label of the appointment type for this event | string
attendees[] | Array of attendee objects | array
attendees[].id | Unique identifier for attendee | integer
attendees[].label | Name/descriptor for this attendee | string
attendees[].type | A valid attendee type (e.g. "individual", "group", "usertype", "year", "position") | string
attendees[].team | Unique identifier for the attendee's team | integer
attending | The attending status of the user (e.g. '', 'attending', 'not attending' | string
creator | The person who created the event | object
creator.id | the unique identifier for the creator | integer
creator.label | The full name of the event creator | string
description | Description of the event | string
duration | The duration of this event in minutes | integer
editable | If this event is editable | boolean
end | an ISO-8601 date time noting the end time of the event, e.g "2016-04-26T13:45:00" | string
id | The unique identifier of the event. | integer
isClass | If this event represents an academic class or not | boolean
label | The label/title of the event | string
location | Where the event will take place | string
mandatory | If this event is mandatory | boolean
private | If this event is marked as private | boolean
recurs | If this is a recurring event | boolean
recurrenceRule | the iCal RRULE, as defined in RFC 2445 which determines how the event recurs | string
reminders[] | Array of reminder objects | array
reminders[].method | The method to use as a reminder (e.g. "sms" or "email") | string
reminders[].minutes | Number of minutes before event to send a reminder| integer
start | an ISO-8601 date time noting the start time of the event, e.g "2016-04-26T13:15:00" | string
timezone | The timezone for the event as specified by the IANA Time Zone Database, e.g. "America/New_York" | string
