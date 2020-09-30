# Feed samples for Jasper 

Here are some examples of feeds that you can create. 

All of these feeds curate content a different way. Some show you posts of dogs, some show you posts your friends have reacted to, some might even show you posts that most people have not seen. 

# Examples

[In Dogs We Trust](https://github.com/elijahleinkram/feed-samples/blob/master/functions/in_dogs_we_trust.js)

[The Road Not Taken](https://github.com/elijahleinkram/feed-samples/blob/master/functions/the_road_not_taken.js)

[FOMO](https://github.com/elijahleinkram/feed-samples/blob/master/functions/fomo.js)

# Why though?

The main idea behind Jasper, is that as consumers of social products, we have missed out on 2 key things. 

1. Transparency as to why posts end up in our feeds. 
2. Control over the algorithms that determine our feeds. 

And at Jasper, we aim to fix that.

# How it works

A [Post](https://github.com/elijahleinkram/feed-samples/blob/master/classes/post.js) enters the feed. The person who makes the post is the [Author](https://github.com/elijahleinkram/feed-samples/blob/master/classes/author.js). The person viewing the post is the [Reader](https://github.com/elijahleinkram/feed-samples/blob/master/classes/reader.js).

Each post has a ranking. The ranking is calculated by the [computeRanking](https://github.com/elijahleinkram/feed-samples/blob/master/ranking/computeRanking) function. The higher the ranking the higher the post will show in the feed. 

You can write your own functions, but the template used must be identical to [this](https://github.com/elijahleinkram/feed-samples/blob/master/ranking/computeRanking). Else, it will not work.

# Rules

If the ranking is less than or equal to zero, the post will be excluded from the feed. 

The feed sorts posts from highest to lowest. That means that if postA has a ranking of 100 and postB has a ranking of 3, then postA will go before postB.

Q. What if they have the same ranking?

A. Then the order will be random.






