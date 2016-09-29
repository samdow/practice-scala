# What's easy to do in Scala? What's not?
It's really easy to do method chaining in Scala. When I needed map, then filter called on only part of a list
I could make all of those method calls on one line and Scala was very okay with it. Additionally, objects 
are very easy to implement in Scala because everything has to be a class already, so making the class some sort
of intersting object is not difficult. With that, inheritence seems to be pretty easy. We only had to use Any for
this assignment. However, from reading the documentation on Sequences and other Collections, it seemed that 
inheritence was very common and calling super methods was simple.

In Scala, it is difficult to learn collection syntax. Although it is simple to use them functionally, with map and
filter, it was very difficult for me to learn the difference between `::`, `+:`, and `++` and some other minor syntax
issues with collections. There were a couple other obscure syntax issues, especially with sumOfMany, which used the *
operator to note that there were many lists. It proved very difficult to find documentation or help on some more
obscure issues of Scala.

# What is/are your favorite language design choice(s) that the designers of Scala made? Why?
My favorite language design choice is the choice to have functional, object oriented programming. I think that they
work really well together. Because of the method chaining that object oriented programming allows, I find it very
readable and easy to parse because everything is in order. I do recognize, however, that this may be my bias from
having a background with programming because a single line with a lot of methods may be more intimidating for a novice
user rather than an experienced programmer.

# What is/are your least favorite language design choice(s)? Why? And why do you think the designers made that / those choice(s)?
My least favorite design choice, apart from having `::`, `+:`, `++`, and `/:` all look so similar was in the Collections
API. I did not like that they did not default `slice` to have the end of the list as its second parameter. I am used to
having languages default the ending of a splitting function be the end of the list. Personally, it confuses me and often
leads to off by one errors because you set the end to be the number after the last element you want to grab. While this
is rather pedantic, I find it confusing and definitely difficult to people without much experience because understanding
that arrays are indexed from 0 but you have to say you want to slice through the length of the list (which is one more than
the biggest index) seems quite confusing.

I think that the designers made this choice so that users would not be confused. If users are coming in from multiple backgrounds
where instead of slicing to the end of the list, the slice function in another language just slices 2 or 3 elements. This
will remind users that it needs to explicitly state where it wants the slice to end to try to help the user debug before
the code has even run. They probably also expect that most languages use indexing from 0 and a slice of this style, where
the last index is one afte the last element you want to get. So, they figure that they will keep with this standard.

# What Scala features would you like to learn more about?
I would like to learn more about inheritence in Scala. We were only able to get a look at it tangentially with respect to Any
and general Collections. I would like to see if it is the same as Java inheritence or if there's anything different, possibly
strange, in Scala's implementation.  
I would also like to learn more about Scala's optimizations. Although Scala is functional focused, I ran into a stack overflow
error during one of the tests from some poorly optimized code. Although I was able to fix the code, the test that it ran seemed
rather short, so I was wondering about what it optimizes for. It's a functional-focused language, so does it focus on recursion?
Or does it think that all the users will use higher-order functions instead of recursion? Based on my albeit short experience, I 
expect that it optimizes for higher-order function.
