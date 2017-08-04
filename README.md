# gid-create-concept

A data component to create concept

    <gid-create-concept user='1' concept='{{concept}}'>
    </<gid-create-concept>
    
The properties 'concept' and 'user' are mandatory.

API endpoint:

    POST /concepts

Input:

- Label of the concept
- List of applications
- LOB Id
- User Id
- List of impact Area

Sample Input: (as JSON payload)

	    {
		"concept": {
		  "label" : "Domain Name",
		  "applications":["app-id-1","app-id-2"],
		  "lob" : "lob-id",
		  "impactArea" : [
				{ 
					"id": "impact-area-id-1",
					"label": "impact-area-label-1",
				},
				{ 
					"id": "impact-area-id-2",
					"label": "impact-area-label-3",
				}
			],
		  "owner" : "user-id"
		}	        
	    }
	
Output:

      {
        "concept" : {"id":"concept-id"}
      }