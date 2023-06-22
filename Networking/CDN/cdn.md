# Content Delivery Network(CDN)

A CDN (Content Delivery Network) is basically a set of servers located at different points of a network that contain local copies of certain content (videos, images, music, documents, websites, etc.) that are stored on other servers, generally geographically distant, so that it is possible to serve such content more efficiently.

This improvement in efficiency is achieved by better load balancing of both the servers that host the content and the links that interconnect the different sections of the network, eliminating possible bottlenecks and serving the data according to the geographical proximity of the end user.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/76ae6800-a792-4498-99d8-8fae8c5fba69">
</p>

The idea is to have a copy of the content close to the user to improve access speed.

In other words, these CDNs replicate content in different networks and countries, directing users' requests to the copies closest to their network. This prevents some servers from collapsing due to excessive requests, thanks to the geographical distribution of the data, and minimizes delays, since the path to the content is as short as possible.

For example, let's suppose that from Madrid we want to watch a YouTube video originally hosted in the USA. We could access it directly along with millions of other users around the world through the increasingly saturated intercontinental links, or we could access a local copy on a CDN server that a company has installed in Madrid, which would improve access speed and reduce latency.

One of the most popular CDNs worldwide is Cloudflare. So when Cloudflare goes down or fails, a huge number of websites go down. Cloudflare acts as an intermediary between the client and the server, using systems called reverse proxies to create copies and caches of websites.

## References
- https://www.cloudflare.com/es-es/learning/cdn/what-is-a-cdn/