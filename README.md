# Strvct
### By Wallscope

## Case in the words of Wallscope
What we ask of you is that you take in this data, work with us to understand the use case
and help us with ideas on how to visualise the vocabulary in a way that makes it easy to
navigate but keeping in mind that the main purpose of the tool is to create and edit the
vocabulary, not just visualise.

## Debriefing
Wallscope creates knowledge graphs from the unique data vocabulary of their clients.
Strvct is a structured data application that helps their clients delivering the right vocabulary to the dataset and visualizing their linked
data. This way, their clients get a better sense of how their data gets structured and improves their understanding of the service and how they should use it.
The way larger datasets get visualized is a tough and challenging concept that wallscope hasn't figured out yet,
so to us the task to help them come up with and prototype ideas for the visualization of LinkedData.

### What does it mean
Starting with this project, I had very little knowledge of LinkedData, knowledge graphs or other of these graph data standards.
To help me understand the assignment a little bit better, I have listed a few terms and standards below that I needed to wrap my head around
first, before I really understood what was supposed to happen.
Most of these terms are mentioned in Medium articles written by employees of Wallscope and are explained lot better and more comprehensive than I did, 
but beneath are my very brief explanations of how I have grasped them.

### LinkedData / knowledge graphs
LinkedData according to W3C:
> The term LinkedData refers to a set of best practices for publishing structured data on the Web. These principles have been coined by Tim Berners-Lee in the design issue note [LinkedData](http://www.w3.org/DesignIssues/LinkedData). The principles are:
> 
> 1. Use URIs as names for things
> 1. Use HTTP URIs so that people can look up those names.
> 1. When someone looks up a URI, provide useful information.
> 1. Include links to other URIs. so that they can discover more things.
>
> The idea behind these principles is on the one hand side, to use standards for the representation and the access to data on the Web.    
> On the other hand, the principles propagate to set hyperlinks between data from different sources.     
> 
> These hyperlinks connect all LinkedData into a single global data graph, similar as the hyperlinks on the classic Web connect all HTML documents into a single global information space. 
> Thus, LinkedData is to spreadsheets and databases what the Web of hypertext documents is to word processor files.
>
> ~ [W3C](https://www.w3.org/wiki/LinkedData)

LinkedData is a term that has been around for quite some time, however these standards are not as widely adopted as Tim Bernsers-Lee had hoped.
It is however becoming more and more popular to use similar standards such as RDF with datasets to work with data.

### RDF
Resource Description Framework, is also a representing data, however it doesn't always requires data to be structured properly.
In the RDF standard, data always consists of what is called a 'triple'.
This means that two datapoints are connected by their relation to each other, so `monkey IS animal` but also `animal CONTAINS monkey`.
The fact that these relations CAN go two ways or even have another relation the other way around is a critical part of why triples are so powerful to represent the data.

RDF accordingf to W3C:
> RDF is a standard model for data interchange on the Web. RDF has features that facilitate data merging even if the underlying schemas differ, and it specifically supports the evolution of schemas over time without requiring all the data consumers to be changed.    
>
> RDF extends the linking structure of the Web to use URIs to name the relationship between things as well as the two ends of the link (this is usually referred to as a “triple”). Using this simple model, it allows structured and semi-structured data to be mixed, exposed, and shared across different applications.    
>
> This linking structure forms a directed, labeled graph, where the edges represent the named link between two resources, represented by the graph nodes. This graph view is the easiest possible mental model for RDF and is often used in easy-to-understand visual explanations.    
>
> ~ [W3C](https://www.w3.org/RDF/)

### OWL
OWL stands for Web Ontology Language, and yes those characters don't line up in the acronym.
I wanted to know whether there was maybe a different acronym it conflicted with or that there was a really profound reason behind the naming, so I started looking.
The first hit was from winnie-the-pooh where an owl supposedly writes his name as 'wol' and I thought I found it, but then I found the OWL faq from W3C

> Actually, OWL is not a real acronym. The language started out as the "Web Ontology Language", but the Working Group disliked the acronym "WOL". We decided to call it OWL. The Working Group became more comfortable with this decision when one of the members pointed out the justification for this decision from the noted ontologist A.A. Milne who, in his influential book "Winnie the Pooh" stated of the wise character OWL: (...)
>
> ~ [W3C](https://www.w3.org/2003/08/owlfaq) 

So a standard for a language that describes ontology for which the name has been chosen on the basis of how much cooler it IS than the original acronym... yeah this is already getting meta.
Actually, OWL is quite a simple concept.

OWL is a way of describing the relations between data.
A perfect example by Antero Duarte of Wallscope in his [Medium article about linkedData](https://medium.com/wallscope/linked-data-a-conceptual-exploration-9860a1f44d68):
> OWL allows us to express that when two people share a parent, they are siblings. So even if our data doesn’t explicitly say that, inference lets us know that the following triples exist implicitly:
> `dbo:Annete dbo:hasSibling dbo:Jackie`
> `dbo:Jackie dbo:hasSibling dbo:Annete`

### What does Strvct do in all of this
Strvct is an application that uses RDF and OWL to represent the vocabulary of a client so they can add NLP features to their products such as semantic search functionality.
The application allows clients to fill in their own data and link their data in a clear and easy to understand visualization.
However, at this point the largest part of Strvct consists of a backend in which wallscope creates the links themselves after a client has send their data in their own format.

### Our goal
Our goal in this is to prototype or atleast conceptualize frontend visualizations for a client so that they can understand what relations exist between which datapoints.
If possible, the way clients enter their data into Strvct and link their data should be taken into account while creating these prototypes.

### Planning
Every week consists of these 4 main tasks
1. Monday - Standup & checkup with our coach and with Wallscope.
1. Wednesday - Codereview from AUAS lecturers Joost & Laurens.
1. Thursday - Designreview from AUAS lecturers Vasilis & Koop.
1. Friday - Prototype testing with Wallscope

The project itself will take up 5 weeks consisting of the following milestones:
1. Debriefing & 1st iteration | Debriefing of the assignment and creating the first prototype/concept
1. 1st & 2nd iteration | Testing the first prototype/concept a total of 2 times (beginning and end of the week)
1. 3rd iteration | Testing the second iteration and working on the third iteration for the rest of the week
1. 4th iteration | This is the last week of testing and after the 4th test, work on the final prototype will start
1. Final prototype | At the end of the week, a final prototype will be presented to Wallscope and all lecturers and students from the webdev program 

With the grasp of the assignment that I have at this point of the assignment, the milestones will probably look like this:
1. Concept & prototype with small dataset | At first I will present a concept to wallscope and get feedback on the concept after which I will commence work on the first prototype to realize the concept with only the smallest dataset provided by wallscope
1. Improvements and larger datasets | When feedback is received on the first prototype, I will implement it into the prototype and start testing with larger datasets
1. Prototype with medium dataset and possibly a peek into a larger dataset | At this point I would want to be able to either show a concept that would scale with the dataset or ideally a prototype that demonstrates this
1. Prototype with large dataset | This will be a continuation of the previous milestone and its feedback
1. Prototype for all datasets | Ideally I will have a prototype or concept that demonstrates well on all types of sizes of datasets
