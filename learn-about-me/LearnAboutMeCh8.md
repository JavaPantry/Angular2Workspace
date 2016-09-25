
## Install project

Install node_modules

    C:\webStormWS\ExpressInAction\Chapter_08\learn-about-me\>npm install

Need additional setup step

    C:\webStormWS\ExpressInAction\Chapter_08\learn-about-me\node_modules\mongodb>npm install


Start mongoDb server

    C:\Program Files\MongoDB\Server\3.2\bin>mongod


Start __Learn-about-me__ project, signup as users admin and alex030365

    C:\webStormWS\ExpressInAction\Chapter_08\learn-about-me>npm start

Run mongo shell

    C:\Program Files\MongoDB\Server\3.2\bin>mongo
    MongoDB shell version: 3.2.9
    connecting to: test
    >
    > show dbs;
    local  0.000GB
    test   0.000GB
    > use test
    switched to db test
    > db.users.find()
    { "_id" : ObjectId("57e82f1fbfd7eba023f4d34b"), "username" : "admin", "password" : "$2a$10$qskNfaPE1/d7OfbvT3dVXu1CYM23F0SZUbxPll8F7pGAS95NqoJWO", "createdAt" : ISODate("2016-09-25T20:10:07.591Z"), "__v" : 0, "bio" : "node scolar", "displayName" : "Alex" }
    { "_id" : ObjectId("57e82f93bfd7eba023f4d34c"), "username" : "alex030365", "password" : "$2a$10$awKAT4MCPCpfF9IC.9xBx.igIsqujbB0ohW5ppdAn6ufAyMd48rOq", "createdAt" : ISODate("2016-09-25T20:12:03.291Z"), "__v" : 0, "bio" : "Basic user profile ", "displayName" : "Alexei" }
    >

end.