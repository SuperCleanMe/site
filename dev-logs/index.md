---
has_children: false
layout: default
title: Dev Logs
nav_order: 3
---

# Development Log - Week 5 {#week-5}

## This post was written by [<img src="https://avatars3.githubusercontent.com/u/63651404?s=60&v=4" width="20px" style="border-radius:25px;">  Thomas B.](https://github.com/fatalcenturion)

### Posted on Monday, January 25th 2021

## Now's your chance to help shape the future of Kalavar! {#week-5-shape-kalavar}

Oh yes, your eyes do not deceive you! Kalavar's dev team is looking for feedback on our configuration system, and we want you to help shape it!

If you want to provide some feedback, take a look at our [reference configuration file](https://github.com/KalavarDB/core/blob/main/sample-config.toml), and then provide some feedback on our [ongoing issue](https://github.com/KalavarDB/core/issues/25)


## Other changes. {#week-5-other-changes}

- Added [documentation for the current config file](https://kalavar.cf/documentation/configuration) ;

- Expanded the documentation for the analytics manager

- Began working on the analytics manager

- Began adding external API for future utilities/"plugins"

- Began refactoring storage manager to accept the transaction model

- Began writing unit tests for individual components

- Added some new features to the dev kit

## Wrapping up {#week-5-wrapping-up}
Changes this week have been primarily preparing for other parts of the project, such as a stats UI of some sort, and planning around our future hopes for Kalavar. We would really appreciate your feedback on our config file.

Thanks for taking the time to read this week's blog post, we look forward to sharing our progress with you in the future!

Like what you see? Star us on [GitHub](https://github.com/fatalcenturion/kalavar-core) to let us know!

-----

# Development Log - Week 4 {#week-4}

## This post was written by [<img src="https://avatars3.githubusercontent.com/u/63651404?s=60&v=4" width="20px" style="border-radius:25px;">  Thomas B.](https://github.com/fatalcenturion) 
### Posted on Monday, January 18th 2021

## We launched a version checker {#week-4-version-checker}
That's right, we spent more than a few hours of dev time on a version checking utility and the Rust community seems to like it! 
The program which is part of our development environment has been made available on [crates.io](//crates.io/crates/version-checker) and it supports checking immediate dependencies, and first-level sub-dependencies. Here is a sample output of the program:
![Sample Output](https://raw.githubusercontent.com/KalavarDB/site/main/assets/images/dev-logs/version-checker-0.1.13.png)

We are incredibly proud of what we have produced with this utility, and we can only continue to make it better in the future

## Developer documentation {#week-4-dev-docs}
On top of the incredibly useful version checking utility, we also launched [dev.kalavar.cf](https://dev.kalavar.cf) which is an automatically updated version of our in-code documentation. This is updated with every push and the idea is that you will be able to use it to learn how things interact within Kalavar's source code.

We hope you find the version checker, and the internal docs useful, we sure will!

Thanks for reading, sorry this post was so short but there really wasn't much to share with you all. See you next week!

Like what you see? Star us on [GitHub](https://github.com/fatalcenturion/kalavar-core) to let us know!

----- 

# Development Log - Week 3 {#week-3}

## This post was written by [<img src="https://avatars3.githubusercontent.com/u/63651404?s=60&v=4" width="20px" style="border-radius:25px;">  Thomas B.](https://github.com/fatalcenturion) 
### Posted on Monday, January 11th 2021

## Nothing major, but still a worthy development blog {#week-3-nothing-but-worthy}
The last 7 days of the project have been littered with a mixture of confusion, stress, and a lot of research. The project ground almost entirely to a halt after to beginning of the 2021 college session, this meant that I had to focus my time on college lectures rather than on Kalavar or any other projects which is unfortunate, but nothing we cannot work around. Lets see how we did this week.

### A major rethink {#week-3-rethink}
I spent a large amount of time asking my developer friends about their opinions on various methods of authenticating users between client and server. One of the ways which was suggested was actually from Reddit's [r/Rust community](https://reddit.com/r/rust), suggested by user [mleonhard in this comment](https://www.reddit.com/r/rust/comments/kqk95q/whats_everyone_working_on_this_week_12021/gihb1iu?utm_source=share&utm_medium=web2x&context=3), the suggestion was to use [mTLS](https://en.wikipedia.org/wiki/Mutual_authentication), a way of dropping passwords for cryptographically generated certificates for a user. This allows us to remove the security risk of database user password leaks, because the server doesnt need to store a password for the users, it challenges their authority during the authentication phase, where they must prove they have both components of the key in order to verify their identity, and perform any actions.
Another thing which mTLS enables us to do, is to encode specific IP addresses into the certificates given to a user, allowing us to check the address in the certificate off against the address they connected from, if both match up then the user is able to connect, if they dont, the user will be denied because of the risk that it may be a third party attempting to gain unauthorised access though a leaked keychain.

### *Bits* and bobs {#week-3-bits-and-bobs}
I also spent a large amount of time working out how to implement storage management for everything from individual table cells, all the way up to entire databases, at once. During this time I came to a rather incredible discovery. Due to the way we intend to store data, there is the potential for a singular row to be up to 16,000 Petabytes in size, with the right hardware. It would take a hell of a long time to process *that* query though, so we obviously dont recommend attempting this at any point.

### Parting words {#week-3-parting-words}
So to summarise, this week we did some research on how to authenticate the identity of a user and validate they are allowed to connect without using passwords, and we also worked on calculating theoretical limitations of the storage management system, as well as beginning to implement said storage system.


Like what you see? Star us on [GitHub](https://github.com/fatalcenturion/kalavar-core) to let us know!

----- 

# Development Log - Week 2 {#week-2}

## This post was written by [<img src="https://avatars3.githubusercontent.com/u/63651404?s=60&v=4" width="20px" style="border-radius:25px;">  Thomas B.](https://github.com/fatalcenturion) 
### Posted on Monday, January 4th 2021

## A busy week, and a few important milestones {#week-2-a-busy-week}
This past week, we achieved a number of first time events, which represent small victories in our battle against the computer to bring Kalavar to the public. First of these milestones was:
### The first inter-process communication {#week-2-first-communication}
This week we achieved the first inter-process communication of our program. This communication was produced by the REPL and CORE components of the database. The REPL component had been heavily modified at the time compared to the build on our [repository](https://github.com/fatalcenturion/kalavar-repl), so naturally, we pushed the build which achieved this to the repository for archival purposes.

### The first inter-thread communication {#week-2-first-thread}
Another major event that happened this week, which we dubbed our "RAMpocalypse". We managed to successfully track the amount of memory our CORE system was using at regular runtime intervals, allowing us to report that to the main system thread for the program. This may seem trivial, but it is a big victory for us in bringing Kalavar closer to production. You may not agree with us, but actually it is the primary method of the program deciding when to move things into and out of system memory to and from the disk.

## Parting Words {#week-2-parting-words}
Although this weeks blog post was a short one, it was always going to be, we've been taking a break over the Christmas period, and although our last post was actually released on Christmas day, our writer had nothing better to do, and so they threw it together for us. Work on the project since the 20th of December 2020 has been slow and uneventful up until this week, and we are hoping to ramp up our progress on the project as soon as we can. 

Thanks for reading this weeks development log, we hope you have enjoyed it!

Like what you see? Star us on [GitHub](https://github.com/fatalcenturion/kalavar-core) to let us know!

<sup>Note: This isnt a guaranteed weekly blog post, it depends on if we have time to write one or if there is sufficient progress to benefit creating one for</sup>
----- 

# Development Log - Week 1 {#week-1}

## This post was written by [<img src="https://avatars3.githubusercontent.com/u/63651404?s=60&v=4" width="20px" style="border-radius:25px;">  Thomas B.](https://github.com/fatalcenturion) 
### Posted on Monday, December 28th 2020

## Meet Kalavar {#week-1-meet-kalavar}

Hi everybody, in this dev log I want to take the time to introduce to you, our little project. We like to call it Kalavar and this is where you read the latest information and developer updates about the system, as we work our way towards a public alpha test release. We hope you enjoy this journey just as much as we will.

## What is Kalavar? {#week-1-what-is-kalavar}
Kalavar is an asynchronous, efficient, and secure database system, programmed using the [Rust](https://rust-lang.org) programming language and built upon the [Tokio](https://tokio.rs/) runtime.

## What does it offer that X does not? {#week-1-offerings}
Kalavar, once ready for a release candidate, will be able to offer a full featured SQL-less query environment, designed to provide asynchronous access to your data, via encrypted data streams. What does that actually mean? well, it means that Kalavar, simply out-classes the competition via the sheer power of asynchronous programming. Queries can be organised and optimised before  being submitted by the client for processing, this allows your queries to be as fast, efficient, and secure as you could ever wish for.

And, on top of this, Kalavar's official clients will also be capable of taking your regular old SQL queries* and transforming them into faster, more efficient KQL queries, before sending them off for processing!

<sup>*SQL transformation limited to PostgreSQL queries. Not all features will be available at time of release. these features will be provided via a downloadable update once they are ready for use</sup>

## Parting words {#week-1-parting-words}
Well, that's it folks, the first developer log is now finished, we hope you enjoyed reading our plans for Kalavar, and we also ask you to keep an eye on this space for more information, as development goes further.

For now though, goodbye from the Kalavar team.

Like what you see? Star us on [GitHub](https://github.com/fatalcenturion/kalavar-core) to let us know!
