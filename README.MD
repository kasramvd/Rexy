## Preamble


*Rexy* (rec-sy) is an open-source recommendation system based on a general User-Product-Tag concept and a flexible structure that has been designed to be adaptable with various data-schema. There are a lot of methods and ways that *Rexy* has used to recommend the products to users. This includes general recommendations like *Top products*, *event based recommendations* and *Novel products* that the user might be interested in. There are other recommendations that are directly related to the user's activities or other users that have a similar behavior to the given user.

Alongside the recommendations that are related to the user's interests, there are also some modules designed to find the most proper products based on other factors like *advertisement*, *social factors*, *gamification*, etc. and don't have the side effects of a commercial advertisement system. `Email` and `Search` modules are designed to support such goals.

The underlying codes are entirely written in Python-3.5 in a highly optimized, *Pythonic* and comprehensive way that makes it so flexible against the changes. It also used [Aerospike](http://www.aerospike.com) as the database engine which is a high speed, scalable, and reliable NoSQL database.

 -----------
 
![tyran nosaurus_rex_t-rex_ 86](https://user-images.githubusercontent.com/5694520/27258385-528b7a66-540e-11e7-8ffd-786cc63a65e8.jpg)

 ----------

 # Structure and Features

*Rexy* is consist of following major modules:



 ![#c5f015](https://placehold.it/15/c5f015/000000?text=+) **Administration**

This module is supposed to handle the administration tasks. But what are administration tasks? In general, these tasks are those that we need for management of the users and products. This can be consist of visualizing the features, extracting a specific information about a user or product, demonstrating the long or short term changes regard a special feature of a given entity or other activities as such.

This module is contain the following submodules:

 - Analyzer

Retrieving and managing the information regard the entities. Such informations, may be used in variant ways such as giving a report to the providers regard their products, finding the popularity of a given product among the users (which can be used in a lot of ways too), estimating the popularity of a new products in our platform, and other purposes as such.

 - Visualizer

Using this module we can do the *Analyzer*'s tasks in a visualized manner. Sometimes we just need to take a glance and figure out a specific information about a particular entity or group of them. In that case *Visualizer* module it what you want.


 ![#c5f015](https://placehold.it/15/c5f015/000000?text=+) **Core** 

 The Core is contain those modules that handle the core operations and might be used in most of the other modules.

 ![#c5f015](https://placehold.it/15/c5f015/000000?text=+) **Email**

This module is designed to handle the recommendations through the *Email*. Emails are basically sent on a weekly/monthly basis, which means that the users have a fewer interaction with. This makes it a proper place for advertisements and going a little bit further than the customized recommendation’s restrictions. Therefore, this module tends to use more diverse and unpopular products in its periodic recommendations.

 Also, in addition to the aforementioned features, in Emails we have more options and space for our recommendations (compare to a profile page which is almost filled with other informations), which makes it possible to involve the new types of recommendations in the future. Hence, this module has been designed in a way to be as flexible as possible against such new changes. 

 ![#c5f015](https://placehold.it/15/c5f015/000000?text=+) **General**

There are also some kind of recommendations that are not specifically personalized for users or products. These are consist of *Novel*, *Top* and *Event* recommendations. The results of these modules, regardless of the subject of the page that we're  planning to show them, can be used for general or personal recommendations. For example, within a home page for everyone or even for not logged-in users on welcome page. 

 - Novel
 
This module is supposed to find the most popular products within a newly certain amount of time. For example, the last month.

  - Top
  
Alongside the Novel products we also need to find the all-time popular products among the users. That's exactly what this module stands for.

  - Event
  
Sometimes we need to go further than regular and common recommendation types, that's where the modules like Event come in. This module finds the most relevant products specially for users and in general, based on the events on a specific calendar. This module has used [Wipazuka](https://github.com/kasramvd/Wipazuka) a multilingual calendar-based WordNet to find the intended products based on events.

 ![#c5f015](https://placehold.it/15/c5f015/000000?text=+) **Logging**

The logging module that keeps track of the errors and exceptions that are happened within the whole application.

 ![#c5f015](https://placehold.it/15/c5f015/000000?text=+) **Profile**

*Profile* is almost the widest module in *Rexy*. It's responsible for every profile in your platform, include *User Profile*, *Product Profile*, *Provider Profile*, etc.

For a given profile we can show a diverse set of recommendations which are as follows:

 - Top Products

Top products of all time, based on user's interest and other purposes.
 
 - Novel Products

Favorite products during the latest N month/week, based on the user's interest and other purposes.

 - Event-based recommendations

Products related to the current events, based on user's interest and other purposes.

 - Recommendations For You

In this part we suggest the products that are based on user's activities or the user's that have similar activities to the given user. Both of these recommendations fall under two accurate and similar categories.

The accurate recommendations are basically based on the common tags among the products. Finding the intersected tags can be done in two level the first one is related to the products that are directly related to the user's products and second one is related to the products that are similar to the similar products of our products.

The similar recommendations are based on the similarities between the common products and similar users in which these similarities are calculated based on the tag densities, common tags, different tags, and some other influential factors. 

 - Top N Picks For You

At this section, we find the *top N products* from all the aforementioned parts.


 ![#c5f015](https://placehold.it/15/c5f015/000000?text=+) **Search**

The search module is responsible for recommendations during the search process by user. Based on user's in case that the searched products are exist in database, we can show the related products based on some manual policies. In case the word doesn't exist in our database, we can use a prepared list of product names which are tagged properly in order to find the related products and show them to the user. This prepared list of products can be a scraped file or something similar. Another way around this is to ask the users to enter/select some related tags to the searched product and find the similar products based on them.

If the user is a logged in user with a history of activity, in case that the searched word doesn't exist in our database, we can recommend a list of products related to the latest users activities top products the most recently searched product, top popular product among the similar users to the user or other different methods.

