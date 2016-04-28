FORMAT: 1A

# Customers [/staff]

## Get customers [GET]
Gets current customers

+ Response 200 (application/json)

    + Body

            [  
               {  
                  "firstName":"Vitaliy",
                  "lastName":"Kuznetsov",                
               }
            ]          

    + Schema

            {  
               "$schema":"http://json-schema.org/draft-04/schema#",
               "id":"/",
               "type":"array",              
               "items":{  
                  "id":"0",
                  "type":"object",
                  "properties":{  
                     "firstName":{  
                        "id":"firstName",
                        "type":"string",
                        "faker":"name.firstName"
                     },
                     "lastName":{  
                        "id":"lastName",
                        "type":"string",
                        "faker":"name.lastName"
                     }                   
                  },
                  "additionalProperties":false,
                  "required":[  
                     "firstName",
                     "lastName"               
                  ]
               },
               "minItems":20,
               "maxItems":30,
               "required":[  
                  "0"
               ]
            }
            
