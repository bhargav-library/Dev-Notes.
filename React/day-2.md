Q) What is Content Delivery Network (CDN)?

A Content Delivery Network (CDN) is a group of servers placed in different locations around the world that work together to deliver website content faster to users. Think of it like this:
Imagine Netflix has only one server in the USA. If someone from India watches a movie, the data has to travel a very long distance, so loading becomes slower. Now imagine Netflix stores copies of that content on servers in many countries, including India. When you open Netflix in India, the content is delivered from the nearest server instead of the USA. That nearby server is part of a CDN.

Q) What does a CDN store?

CDNs mainly store: Images, Videos, CSS files, JavaScript files, Fonts, Website pages, App downloads. These are called static assets.

Q) Uses of CDN?

1. Faster Website Loading: A CDN sends data from the closest server to the user, reducing distance and loading time. For example if there were no cdn then only one sever which can be anywhere in the world would had to serve all the countries which could have lead to crashing an application but with cdn which are alomost everywhere will lead to faster application loading.
2. Reduces Load on Main Server: Instead of millions of users hitting one server, the traffic gets distributed across many CDN servers. This prevents: Server overload, Crashes during heavy traffic.
3. Better Performance During High Traffic: Websites like, Amazon, YouTube, Facebook use CDNs because millions of users access them simultaneously.
4. Protection Against DDoS Attacks: A CDN can absorb huge amounts of fake traffic and protect the original server. This improves security.
5. Improves Availability: So, websites remain online even during failures. If one CDN server fails, another nearby server can still deliver content.
   
Q) What is Cross Origin?

 The cross origin attribute in the script tag enables Cross Origin Resource Sharing (CORS) for loading external JavaScript files from different origin than the hosting web page. This allows the script to access resources from the server hosting the script, such as making HTTP requests or accessing data.
 
Q) What is {} denotes in react?

classes should come under {}. Whenever we are passing inside {}, will go as tag attributes of h1.

Q) What is the difference between `react.development.js` and `react.production.js` files via CDN?

`react.development.js` is the version of React that is used while developing an application. This version contains human-readable code, which makes debugging easier for developers. The file is not compressed, and React provides detailed warnings and error messages that help developers identify mistakes and reduce bugs during development. However, this version also has some drawbacks. Since it contains debugging tools and extra developer warnings, the file size becomes larger. It is also slightly slower because React performs additional checks in the background.

On the other hand, `react.production.js` is the version used in real or live websites. This version is optimized for speed and performance because all unnecessary development checks and warnings are removed. The code is compressed and minified, which reduces the file size and improves loading speed for real users. However, this version also has some disadvantages. It does not provide detailed warning messages, and debugging becomes harder because the code is compressed into very small unreadable lines.

So, during development we usually use the development version of React because it helps in finding bugs and understanding errors easily. Later, when the application is fully developed and ready for deployment, we replace the development CDN link with the production CDN link for better performance and faster loading speed.


