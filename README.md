# pyd2r
Python Data Service Server

This program takes an input JSON string describing a database query and exposes it as a rest interface

```
{
  "DBType": "mysql",
  "DBHOST": "localhost",
  "Name": "getCust",
  "ops": [
    {
      "endpoint: "custname",
      "method": "GET",
      "statement": "SELECT fname,lname FROM user WHERE fname like %1"
      "values": [
        { 
          "name": "fname",
          "type": "string",
          "location": "url"
    }
  ]
}
```

Would expose a rest enpoint @ http://yourserver/pyd2r/getCust/{fname} 



