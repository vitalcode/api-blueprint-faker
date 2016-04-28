FORMAT: 1A

# Customers [/customers]

## Get customers [GET]
Gets current customers

+ Response 200 (application/json)

    + Body

            [  
               {  
                  "firstName":"Vitaliy",
                  "lastName":"Kuznetsov",
                  "address":{  
                     "streetAddress":"24",
                     "streetName":"21 2nd Street",
                     "city":"New York",
                     "country":"USA"
                  },
                  "phoneNumber":[  
                     "07999999033"
                  ]
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
                     },
                     "address":{  
                        "id":"address",
                        "type":"object",
                        "properties":{  
                           "streetAddress":{  
                              "id":"streetAddress",
                              "type":"string",
                              "faker":"address.streetAddress"
                           },
                           "streetName":{  
                              "id":"streetName",
                              "type":"string",
                              "faker":"address.streetName"
                           },
                           "city":{  
                              "id":"city",
                              "type":"string",
                              "faker":"address.city"
                           },
                           "country":{  
                              "id":"country",
                              "type":"string",
                              "faker":"address.country"
                           }
                        },
                        "required":[  
                           "streetAddress",
                           "streetName",
                           "city",
                           "country"
                        ],
                        "additionalProperties":false
                     },
                     "phoneNumber":{  
                        "id":"phoneNumber",
                        "type":"array",
                        "minItems":1,
                        "maxItems":5,
                        "items":{  
                           "id":"0",
                           "type":"string",
                           "faker":"phone.phoneNumber"
                        }
                     }
                  },
                  "additionalProperties":false,
                  "required":[  
                     "firstName",
                     "lastName",
                     "address",
                     "phoneNumber"
                  ]
               },
               "minItems":20,
               "maxItems":30,
               "required":[  
                  "0"
               ]
            }
            
