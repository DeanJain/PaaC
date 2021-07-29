---
marp: true
title: Application Caching
description: Application Caching Presenation on Markdown
theme: gaia
size: 16:9
paginate: true
_paginate: false
header: ":copyright: OSS"
footer: "PaaC Rocks :blue_heart:"
---

![bg](./assets/gradient.jpg)

# <!--fit--> Application Caching

Application Caching Presentation Using Markdown

<style scoped>a { color: #eee; }</style>

<!-- This is presenter note. You can write down notes through HTML comment. -->

---
![bg](#123)
![](#fff)
#### Agenda
- Introduction
- Summary - The What
- Features - What All
- The How
- The Why -> Pros and Cons
- The When and where
- Another How (to Get Started)
- References (From Where)

---

#### Intro
- Enable app layer in memory caching which can be used by any API / frameworks to cache data, and improve latency and load on DB

- Integrate distributed embedded caching with our existing application with simple annotation in our spring applications
---

![bg](#123)
![](#fff)

#### Features:
- Easily integrate with JPA/Hibernate
- Support for Relational DB / Joins
- Support for TTL
- Support for Cache - Aside strategy
- Light weight and fits into small - pods
- Minimal setup needed / Easy to use - learn
- Distributed Caching - ideal case without a dedicated server

---

### Application Caching:
There are two patterns of caching the data in application caching.

1. ##### Caching Database Queries: 
- This is the most commonly used caching pattern. Whenever you query your database, your store the result dataset in the cache. Each result dataset will have a hashed version of the query as the cache key. 
- Every time you run the query, you first check if cache-key is already in the cache. 
- If it’s in the cache return it from there otherwise fetch the result from the database and store the result dataset in the cache for future queries. 
- The main issue with this pattern is the cache invalidation. It is hard to invalidate the cached result when you cache a complex query result. When one piece of data changes (for example, a table row) we need to invalidate all cached queries which include that row.

<style scoped> { font-size:24px;}</style>

---
![bg](#123)
![](#fff)

2. #### Caching Objects: 
- In objects caching pattern, you store the data as an object as you do in your application code (classes, instances, etc.). 
- Your class can assemble a dataset from your database and then you can store the instance of the class or the assembled dataset in the cache. 
- Some examples of objects that can be cached are User Sessions, Fully Rendered Web pages, Activity Streams, User Graph Data.

---
### Caching Update Strategy:

1. Read-Through
- In cache-aside, the application is responsible for fetching data from the data store and populating the cache. In read-through, this logic is usually supported by the library or stand-alone cache provider.
- Unlike cache-aside, the data model in the read-through cache cannot be different than that of the database.
- Read-through cache also works best for read-heavy workloads. 
- Read-through cache strategy is quite similar to cache-aside accept instead of managing both data store and the cache, delegates data store synchronization to the cache provider
- Both cache-aside and read-through loads data lazily on the first read.

<style scoped> { font-size:28px;}</style>
---

![Marp bg 90%](https://miro.medium.com/max/1145/1*b2t2aF7ODiI-DovHGUc7Kw.png)

---
![bg](#123)
![](#fff)

- ### What do you guys think :ok_hand::blush:
- ### Discussion :hand::unlock:
- ### Questions :question::bulb:
---

![bg 40% opacity blur](https://avatars.githubusercontent.com/deanjain)

##### Created by Dean Jain ([@dean.jain](https://github.com/deanjain)) 

<br /><br /><br /><br /><br /><br />
<br />

Powered by PaaC (Presentation as a Code) :heart::purple_heart::green_heart::blue_heart: