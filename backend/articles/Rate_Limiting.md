# Rate Limiting
Notes from this article: [Link](https://blog.bytebytego.com/p/rate-limiting-fundamentals?utm_source=post-email-title&publication_id=817132&post_id=124962528&isFreemail=true&utm_medium=email)

1. What is rate limiting?
    1. Controls the rate at which users or services can access a resource, like an API, a service, or network
2. Benefits
    1. Prevents resource starvation (DoS attacks)
    2. Reduce cost (limit calls to control cost)
    3. Prevent servers from being overloaded
3. Applications of rate limiting
    1. Commonly applied on user level -> ie popular social media platform - block users from number of posts or comments
    2. Application level -> ie ticketing platform - limit number of ticket purchases per minute 
    3. Api level -> ie limit number of API calls each user can make per min
    4. Account level -> ie SaaS company - has diff tiers of service with diff usage rates
4. Core concepts of rate limiting
    1. Implementations: Limit, window, identifier
        1. Limit - ceiling for allowable reqs/actions within designated time span
        2. Window - time period limit comes into play
        3. Identifier - unique attribute that differentiates between individual callers (ie user ID, IP)
    2. Responses: Blocking, throttling, shaping
        1. Blocking - takes place when reqs exceeding the limit are denied access to resource (ie 429 HTTP code)
        2. Throttling - involves slowing down or delaying the req that go beyond the limit
        3. Shaping - allows the reqs that surpass the limit, but they get lower priority
5. Common rate limiting algos [Can read on diff rate limiting algos here](https://nordicapis.com/different-algorithms-to-implement-rate-limiting-in-apis/)
    1. Fixed Window Counter
    2. Sliding Window Log
    3. Sliding Window Counter
    4. Token Bucket
    5. Leaky Bucket

