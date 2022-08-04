# JsonReplaceDataHandler
This code will replace the data at any depth programmatically. To understand this code please go through Read me of JsonPathHandler Repo.

This code takes two input parameter. First is the reconciled single level Json containing key as the path of your multi level json (Which can be genearted from Json Handler repo code) and Values as reconciled values (The values you wanna change). Second parameter is your complex multi level json.

Let us take the same example from Json Handler repo. If the complex json is like - 
{
  "Username": "Bob",
  "Address": {
    "Street": "19th main",
    "House no": 80,
    "Locality": "HBR",
    "pincode": 560034
  },
  "phone": 83095
}


And you want to change the values at any depth for example - Change the Username, House no and pincode then use this code and pass the first parameter (Can be generated using JsonHandler code) as

{
  "/Username": "Ross",
  "/Address/pincode": 560089,
  "/Address/House no": 200
}  

Second Parameter is your complex json that is on the top.

your Output will be 

{
  "Username": "Ross",
  "Address": {
    "Street": "19th main",
    "House no": 200,
    "Locality": "HBR",
    "pincode": 560089
  },
  "phone": 83095
}

NOTE - This code can handle any level of JSON wether it be JSON Array or Object.
