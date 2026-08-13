# migrated-express-app - Activity 4

How many lines of code did you eliminate by migrating to Express?
> I think it is around 80 lines of code just by migrating to Express

What was the most surprising thing that Express handled automatically?
> It is much easier to navigate the code and it doesn't use fs anymore since it uses Express and CORS.

Why is `express.static()` better than manually using `fs.readFile()`?
> With `fs.readFile()` I had to code every file one by one and fix errors. With `express.static('public')`, one line is enough to show all my frontend files.

If you had to add a PUT route to update a task, how would you write it in Express? (Write a short code snippet.)
>I dont really know much but i will try to do it on my own next time.

What is one disadvantage of using a framework like Express? (Hint: think about dependencies, learning curve, or abstraction.)
>> My native app had no `node_modules`, but Express added many files. It also hides how Node really works, so I have to install Express to make it work.
