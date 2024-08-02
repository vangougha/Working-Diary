## Day 1

I studied for 2 hours and i learned about the basics of ASP.Net Core MVC(HTML rendering, @model etc...).

I also transformed my Steam-Api console app to web app using documents and help of my friends.

## Day 2

I studied for 1 hour and I learned about Model Binding and explanation of Controller and View's.
I created my first project and thats about applying to courses.
And i learned about [ValidateAntiForgeryToken] ,[HttpPost], GET,POST and what [FromForm] stands for.
I also created a simple login page with a form and a button. I used the [ValidateAntiForgeryToken] attribute to prevent cross site scripting.
When I complete course I'll code a To-Do App with a real database for myself.

## Day 3

I started studying at night and I write these at that time. I set up a feedback mechanism, I learned the repository, taghelper and prepared the "Applications" page, which will return the data entered by the user in a way that will be available to other users. Also I added Feedback system, so when you apply you get a reply that says "You're accepted" and I also learned about Model Validation.

## Day 4 
I studied Data-driven programming using SQLite3 2 hours straight and I learned more than I know about migrations. I created a Database using SQLite and PowerShell about "Product"'s and take some notes 
The notes I took : 
1 - 
        I already have a migration, I'll update it.
        dotnet ef migrations add ProductSeedData
        
2 - 
        It returned all datas
         sqlite> select * from Products ;
┌───────────┬─────────────┬─────────┐                
│ ProductId │ ProductName │  Price  │
├───────────┼─────────────┼─────────┤
│ 1         │ Computer    │ 17000.0 │
│ 2         │ Ipad        │ 17000.0 │
│ 3         │ Table       │ 1000.0  │
│ 4         │ Phone       │ 17000.0 │
└───────────┴─────────────┴─────────┘

3 - 
         It say's to app "Add some service support, service = .... for example if I was working with API's i could say "AddController" or something 
         //I did that because i wanted to add view and controller at the same time.
builder.Services.AddControllersWithViews();

// My ConnectionString is ready
builder.Services.AddDbContext<RepositoryContext>(options =>
{
    options.UseSqlite(builder.Configuration.GetConnectionString("sqlconnection"));
});

// When you do that service service registration you can use it with middleware
