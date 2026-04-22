The data teams of today operate by stitching together tools that is supposed to deliver the data outcomes. With the entire unbundling movement of data stack (https://roundup.getdbt.com/p/bundled-or-unbundled-data-stack - A good article detailing the unbundling movement of data stack), in the last decade of an explosion in the number of data tools has happened. For me, this explosion was fascinating, as this was the data people’s opportunity to do what other people did with “craig’s list”. 

# The MAD landscape

It was 2017, when I first came across MAD landscape by Matt Turck. It was called "Big Data Landscape" then and I was able to see the set of companies which were building the data tools of my dream. To be frank, I was enamoured by Snowflake at that point and was following every piece of information during that time.  What was even more fascinating was the spread of companies that opened this whole new world for me to explore. 
In 2017, that landscape had about 700 odd tools spread across 70 different categories. Most of these tools were not even pure play data tools. Fast forward to 2024, we now have a massive spread of more than 1000 companies in more than 100 categories. I gave up counting to get the accurate numbers and that's the exact point I am trying to make. It's a lot of tools competitive for the attention of the data teams. So MAD is very apt description, I would say.

# What is the question?

So the question I keep asking myself is this - ***"Do the data teams really need this many tools to deliver outcomes?"*** 

There were multiple ways to try and answer the question and the one I chose was the "Needs and Wants" approach. Which tools are absolutely required by data teams and which are the tools that they want but can still deliver successfully without the wanted tools. This is very important because one of my core hypothesis has been that data teams have essentially become white elephants, which are not able to justify the massive investment that it requires. As Gartner had shared in 2023 in Gartner summit, 69% of data teams are not able to justify the investments made.

# What are the needs of the data team?

In my opinion, any data strategy boils down to 5 components - Ingest, Store, Process, Serve and Govern. Any complex data architecture diagram can more or less compressed into these 5 boxes and have a great data strategy. If a data team wants to deliver value, all they have to do is cover these 5 areas and they will be able to show success.
So a typical data team needs 5 tools - 1 ETL tool, 1 storage, 1 processing engine, 1 BI tool and 1 data governance practice (excel would suffice to start with!). So extending this thought, a typical data stack would look like Airbyte + S3 + Spark + Spreadsheet. With this simplified stack, most data teams will be able to solve the 90% problems posed by data teams.

![[Data Stack Basic 1.png]]

You could mix and match with other tools, but the point being that this is the foundation on which you could solve most problems and here on out, it's a matter of asking the question - Why? Every additional component added to this foundation drastically increases the complexity and you will either have to invest hard money or develop skills. Both are time consuming exercises.

I am not at all making the argument that there is no need for further complexities, but it needs to be done with intention and managed by mapping to a clear outcome. Otherwise, you will run into massive costs that will be difficult to justify.

# What are the wants of the data team?

Once your 90% use cases are solved, every single step increase for the data team comes at significant cost. To deliver these step increases, there are many tools and processes that needs to be built and here is where the wants comes in.

Data teams will very soon realize that they want a fancy tool for governance and monitoring. They will start "wanting" a fancy tool which bring all the different tools current being used into a unified view. This list is endless and I have not even started on the complexities involved by the different service models.

If your outcome is AI + ML, then the service models will change drastically as the number of touch points explode at this point. What if this is a data product based service model? Again, the number of wants balloons.

# Conclusion

Long story short, I will say my favorite line - "It depends". 
1. It depends on the scope that the data team wants to take upon itself while solving business problems. I mean, data teams have to solve a business problem - directly or indirectly. Otherwise, you would have invested millions without a good answer to the value that was added.
2. It depends on How mature is the business in terms of it's data expertise and usage. A business that defines itself as "data first" should have reached certain maturity level.
3. It depends on what type of business it is. If it's a new age AI based business model, then your data stack will become very complex very fast with large data team required to support it. But if you are into selling consumer goods, then complex data architectures will be very difficult proposition.
4. It depends on how good a data team exists within the company. Without good data folks, it's a bottomless pit for money.