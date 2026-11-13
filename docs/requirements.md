# Requirements

## User Needs

As  a bristol resident, i want to select my neighbourhood and view its health statistics so that i can understand the health of my local community. 
As a student or resarcher, i want to access health statistics from different bristol neighbourhoods so that i can analyse differences in community health for resarch purposes 
as a community or health organisation, i want to compare health statistics between bristol neighbourhoods so that i can idenitfy areas that may need additional health support 
As a bristol resident, i want to xompare my neighbourhoods health statistics with bristol average so that i can understand how my area compares with the wider city 
As a student or researcher, i want to explore the individual health indicators so that i can understand specific health issues affecting different neighbourhoods 

### Actors
Bristol residents - The primary users of bristolPulse who wants to understand health statistics for their local neighbourhood 
Student/researcher - A secomndary user who accesses health statistics to support research and analyse differences between the neighbourhoods. 
Community/Health organisations - A secondary user who uses local health info to understand community health needs and identify areas that may require additional support.

### Use Cases

case 1 - use case iD and Name - Select a bristol neighbourhood 
Description - Allows users to select a Bristol neighbourhood to access health information about that area. 
Actors - Bristol resident, Students, health org
Assumptions - The user can access the BristolPulse app and the availble neighbourhood list has been loaded. Post condition; the selected neighbourhood is displayed.
Steps - 1: user opens Bristolpulse, 2: System displays available bristol neighbourhood 3:user selects a neighbourhood 4: System processes the selection 5: system displays the selected neighbourhood and its available information.

variations - If the selected neighbourhood is unavailable, the system displays an appropriate error messages and allows the users to select another area. 
non Functional - The neighbourhood selection shoudld be simple, accessible and easy to naviagate.
issues - the final neighbourhood list must list match the geographical areas available in the chosen dataset.

Case 2 - Use case id and Name - View Neighbourhood health statsitics
Desriptions - Allow users to view health statistics for their selected bristol neighbourhood, including life expectancy , smoking rates , long term health conditions and premature deaths where data is available.
Actors - bristol resident , student/ Researchers, health org
Assumptions - The user has selected a neighbourhood and the relevant health statistics are available. post-condition: The selected neighbourhoods health statistics are displayed.

steps : 1-user selects a neighbourhood. 2- User chooses to view health statistcs. 3-system retrieves the relevant statistics from its dataset. 4-system organises the information into clear sections. 5- user views the health statistics.

Variations - If information is missing for a particular indicator, the system displays an unavailable data message instead of showing an incorrect value 

Non functional - health info must be presented clearly , accurately and consistently.

issues - The availablity of each health indicator depends on the selected dataset

case 3 - Compare neighbourhood Health statistics 
 use case id and name - Compare neighbourhood health statistics
 description - Allows users to compare the health statistics of a selected neighb ourhood with the bristol average to understand differences in community health 
 
 Actors - Bristol resident, student, community/health org
 
 Assumptions - The selected neighbourhood and bristol average have comparable heslth statistics available. post condiiton: the comparison is dispalyed to the user

 Steps - 1:user selects a bristol neighbourhood 2:user chooses the comparison option 3:System retrieves the selected neighbourhoods statistics 4: system retrives the corresponding bristol average 5: system compares the available figures 6: system displays the comparison.

 Variations - If a comparablble bristol average is unavailble, the system informs the uer and displays the available neighbourhood statistics 

 Non funtional - comparisons must be clear, accurate and use consistent units and reporting periods 

 issues - some health indicators may not have directly comparable meighbourhood and bristol wide figures.


TODO: Your Use-Case diagram should include all use-cases.

![Insert your Use-Case Diagram Here](images/usecase.png)

## Software Requirements Specification
### Functional requirements
FR1 The system shall display a list of available bristol neighbourhoods. - UC1

FR2 the system shall allow users to search for specific bristol neighbourhood UC1

FR3 the system shall allow users to select a neighbourhood to view its health information UC1

FR4 The system shall retrieve health statistics for selected neighbourhoods, including life expectancy, smoking rates, long term health conditions and premature deaths - UC2 

FR5 the system shall display the health stats for the selected neighbourhood  UC2

FR6 The system shall retrieve the bristol wide avg health stats for comparison UC3

FR7 the system shall allow users to compare the selected neighbourhoods health stats with the bristol avg UC3

FR8 the system shall display available trend in health stats over time UC3

FR9 The system shall allow users to explore individual health indicators UC4

FR10 The system shall present health info using graphs and charts UC4

FR11 The system shall display key insights to help users understand the health info UC4


### Non-Functional Requirements
NFR1 - Usability ( people should find BristolPulse easy to use ) 
quality attribute : usability
use case - UC1. UC2
The system shall shall have a simple and easy to undersatnd interface so that users can select a bristol neighbourhood and view its health statistics without difficulty 

NRF2 - Perfomance ( health stats should load quickly)
Quality attribute : Efficiency
use case - UC2,UC3
The system shall display the requested health statistics within 5 seconds under normal internet and API conditions 

NFR3 - Reliability (the app should handle API errors properly)
Quality attribute : Reliability
Use case : UC2, UC3
The system shall display a clear error message if the bristol open data API is unvavailable or the requested data cannot be retrieved 

NFR4 - Accessibility (text, colours and navigation should be easy to use )
Quality attribute : Usability 
use case : UC1, UC2, UC3
The system shall use readable text, suitable colour contrast and clear navigation to make the application accessbile to users with different needs 

MFR5 - Compatibility ( The app should work across common browsers )
Quality attrubute - Portability 
Use case : UC1, UC2, Uc3

the system shall work correctly on the latest versions of commonly used web browsers, including google chrome, microsoft edge, safari. 
