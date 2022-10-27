# OOP in JS

> আমার মতে **constructor** হচ্ছে **object** বানানোর নানা রকম পদ্ধতি। ৪ ভাবে আমরা **object** বানাতে পারি,
>
> > function এর সাহায্যে
>
> > class এর সাহায্যে
>
> > Object.create() এর সাহায্যে

## functional constructor

> **functional constructor** এ আমরা function delcalration এর মাধ্যমে Object এর blue-print create করি এবং পরে একটা variable এ **new** keyword এর সাহায্যে **instantiate** করে নতুন object create করে থাকি। আর যেহেতু **functional constructor** এ **instantiate** করার সময় automatically **Object** construct হয় তাই আমাদের **constructor** keyword use করতে হয় না যেটা **Class Constructor** এ অবশ্যই দরকার পরে

```http
filepath: OOP.js
""""""""""""""""

//Basic Obj in JS
const obj = {};

obj.name = "code ABC";
obj.model = "mdl-25k";

console.log(obj)


//Functional Constructor for creating objects
const Computer = function(name, model) {
    this.name = name;
    this.model = model

    this.aboutComputer = function() {
        console.log(`this computer name is ${this.name} and the model is ${this.model}`)
    }
}

const dell = new Computer("dell", "dkl25");
console.log(dell)
dell.aboutComputer()
```
