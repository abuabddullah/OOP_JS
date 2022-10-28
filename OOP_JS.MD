# OOP in JS

> আমার মতে **constructor** হচ্ছে **object** বানানোর নানা রকম পদ্ধতি। ৪ ভাবে আমরা **object** বানাতে পারি,
>
> > function এর সাহায্যে
>
> > class এর সাহায্যে
>
> > Object.create() এর সাহায্যে

## functional constructor

> > functional constructor এ আমরা function delcalration এর মাধ্যমে Object এর blue-print create করি এবং পরে একটা variable এ new keyword এর সাহায্যে instantiate করে নতুন object create করে থাকি। আর যেহেতু functional constructor এ instantiate করার সময় automatically Object construct হয় তাই আমাদের constructor keyword use করতে হয় না যেটা Class Constructor এ অবশ্যই দরকার পরে

## Prototype

> > যেকোন arrayকে যখন declare করা হয় তখন এর ভিতরে automatically বেশ কিছু default functions (filter,map,foreach,find,concat etc..) prototype এর ভিতরে থাকে যা নরমালি array এর element হিসেবে show করে না কিন্তু যখন দরকার সরাসরি ডট(.) এর পরে use করা যায় । আবার আমরা চাইলে এই prototyper এর ভিতরে যেকোন functions কে modify করে তার default behaviour কে change ও করতে পারি

## prototype chaining

> > যদি কখনো এমন দরকার পরে যে আমাদের parent এর সকল protoType এর access তার সাপেক্ষে তৈরিকৃত object এর মাঝে দরকার তখন আমরা proto chaining এর মাধ্যমে kid এ (.**proto**) inherrite করতে পারি কিংবা আমরা চাইলে default Object() function use করে কোন নির্দিষ্ট object অথবা array এর অভ্যন্তরিন prototype কে inherrite করতে পারি

## class Constructor

> আমরা যখন class এর সাহায়ে কোন object create করি তখন parent blur-print এর ভিতরে constructor() method কে define করে দিতে হয় যেটাই মূলত object-body আর এর ভিতরে যা যা থাকে(key-value,method,console) সবে instantiating এর সময় automatically call হয়ে যায়। আর এর বাহিরের যত কিছু সেগুলা prototype হয়ে যায়
>
> > class constructor এ আমরা বিভিন্ন রকম custom methods define করতে পারি যেগুলো আমরা যখন যখন চাই তখন তখন কল করতে পারি।
>
> > class constructor এ কিছু default method থাকে যেমন static,getter,setter,extends,super,constructor ইত্যাদি।
> >
> > > static method কেবল মাত্র class এর ভিতরে কল করা যায়। এবং এই static method কেবলই parent এর সাথে accessible হয়।
> >
> > > getter এবং setter এর মাধ্যমে আমরা কিছু কিছু কে প্রকাশ করতে পারি এবং কিছু কিছু কে পরিবর্তন করতে পারি। তবে এদের কে use করার সময় function এর মত করে use করা যাবে না বরং object chaining এর মত করে use করতে হবে।

## inherritence

> ধরুন আমার বাবার ২৫ শতক জায়গা আছে যেটা আমি উত্তরাধিকার সূত্রে পেয়েছি তার পাশাপাশি আমি আরো ৫ শতক কিনেছে তাহলে আমার ছেলে উত্তারাধিকার সূত্রে মোট ৩০ শতক পাবে এই জিনিসটাকে যদি আমি object এ define করতে চাই তাহলে আমি class constructor এর extends,super ইত্যাদি methods গুলো use করব নিচের মত করে
>
> > এখানে extends method abdullah কে তার বংশ জন্ম পরিচয় বলে দিচ্ছে আর super method এর সাহায়ে সে তার বাবার থেকে আমার উত্তারাধিকার সম্পদ বুঝে নিচ্ছে ।

## basic terms of OOP

> OOP এর 4 টা basic terms আছে inherritence,abstruction,encapsulation,polymorphism । যার মাঝে inherritence টা আমরা already আগেই বুঝে গিয়েছি আর এখন বাকি 3টা নিচে বুঝব,
>
> > abstruction : আমরা যখন কোন project বানাই তখন আমরা অনেক অনেক coding implement করি যা আসলে user এর কোন কাজেই আসে না যাদের low level programming work বলে এই সব operational functionality গুলোকে smartly hide করে যাওয়া আর কেবল usefull functionality গুলোকেই তুলে ধরা কেই abstruction বলে
>
> > encapsulation : কোন কোন সময় আমাদের কিছু private varibale,method আমাদের দরকার পরে যা আমরা কেবল parent class constructor এর মাঝেই accessible হিসেবে চাই এর বাইরে বা child class এ এদের access দিতে চাই না এই সব ক্ষেত্রে আমরা #varibale or #method ব্যবহার করে এই কাজটা করতে পারি । এই ঘটনাকেই encapsulation বলে। <br/>
> > তবে আমরা যদি parent class এর কোন shared method or variable এর সাথে এই private variable or method কে call করি তখন কিন্তু তা আবার child class এ দেখানো যাবে
>
> > polymorphism : parent class এর কোন function কে নিজের প্রয়োজনমত modify করে child class এ itroducce করানোকে polymorphism বলে
