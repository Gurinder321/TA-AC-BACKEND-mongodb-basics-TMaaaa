db.articles.insertMany([
{
title: "Title One",
createDate: new Date("2018-03-03"),
details: "Lorem ipsum Lorem ipsum Lorem ipsum",
authors: { name: "abc", email: "abc@gmail", age: 25 },
tags: ["js", "mongo"],
},
{
title: "Title Three",
createDate: new Date("2012-03-03"),
details: "Lorem ipsum Lorem ipsum Lorem ipsum",
authors: { name: "abc", email: "abc@gmail", age: 25 },
tags: ["php", "flask"],
},
{
title: "Title Two",
createDate: new Date("1932-03-03"),
details: "Lorem ipsum Lorem ipsum Lorem ipsum",
authors: { name: "Tina", email: "tina@gmail", age: 21 },
tags: ["react", "vue", "angular"],
}
]);

db.articles.find(ObjectId("624c58e0e45b2de0c86f90d2"));

db.articles.updateMany({}, { $rename: { details: "descriptions" } });

db.articles.update({ title: "Title One" }, { tags: [
"js",
"mongo",
"Johnny dodo"
]});

Update an article's title using $set and without $set.

Write the differences here ?
With $set - the command only changes the the value in that particular key
without $set - the command overwrites everything is that command
