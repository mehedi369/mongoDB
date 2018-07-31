# Connect with Mongoose
##### In order to Connect with mongoDB we need to have mongoose(A node-package-module).After that we nedd to follow some steps for creating and finding data in mondoDB.
````
// Importing mongoose to our application
const mongoose = require('mongoose');

// Connect with the running DB
mongoose.connect("mongodb://localhost:27017/oppo", { useNewUrlParser: true });

// making Schema or Plan for phones database or Pattern
let phoneSchema = new mongoose.Schema({
    name: String,
    price: Number,
    seller: String
});

// Making the model of the DB
let Phone = mongoose.model("Phone", phoneSchema);

/* All of that are commented because each time we run the program we will add that Schema or model.

// adding a new cat in the database
let oppo = new Phone({
    name: "Oppo A2",
    price: 200,
    seller: "Arafat"
});

// Saving the data in the DB
oppo.save((err, phone)=>{
    if(err){
        console.log(err);
    } else {
        console.log("We just saved a new phone in DB.");
        console.log(phone);
    }
});

*/

// Alternative method of creating Objects on the DB

Phone.create({
    name: "oppo a3",
    price: 400,
    seller: "Mithu"
}, (err, phones)=>{
    if(err){
        console.log(err);
    } else {
        console.log("DB of new Phone and Seller");
        console.log(phones);
    }
});


// retrieving all cats from the DB using console.log

/*
Phone.find({}, (err, phones)=>{
    if(err){
        console.log(err);
    } else{
        console.log("All the phones");
        console.log(phones);
    }
});
*/
```
