# Friday morning projects at Hacker School

## Week 2 - Phonebook command line tool

Written in Julia. I'm not used to writing code where ease of testing drives design, so spent most of my time thinking about how I feel about that.

### Status:
* It took a while to realize the functions that generate output for the command line shouldn't be printing it themselves -- this tightened things up considerably.
* Alan convinced me that those functions should take a phonebook rather than a phonebook name -- which didn't seem natural because without opening and saving books, there's not much left, but apart from speeding tests, it would be much more flexible, for example...
* It would be nice for `phonebook mybook.pb` to hold a book open and subsequent commands to work on that book until it's closed.
* I didn't consider it for something so simple, after Alan got me thinking about it by bringing up command line parsing, I think it might already make sense to use [ArgParse.jl](https://github.com/carlobaldassi/ArgParse.jl).
* I used the base Julia testing functionality, because that's what I've used working with the Statistics packages, but I'd like to look through the various testing frameworks before next Friday's project.
