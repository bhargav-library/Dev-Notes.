Q) What is Content Delivery Network (CDN)? and What are its use cases?
A Content Delivery Network (CDN) is a group of servers placed in different locations around the world that work together to deliver website content faster to users. Think of it like this:
Imagine Netflix has only one server in the USA. If someone from India watches a movie, the data has to travel a very long distance, so loading becomes slower. Now imagine Netflix stores copies of that content on servers in many countries, including India. When you open Netflix in India, the content is delivered from the nearest server instead of the USA. That nearby server is part of a CDN.
Q) What does a CDN store?
CDNs mainly store: Images, Videos, CSS files, JavaScript files, Fonts, Website pages, App downloads. These are called static assets.
Q) Uses of CDN?
1. Faster Website Loading: A CDN sends data from the closest server to the user, reducing distance and loading time.
Example: Without CDN → Server in USA serves Indian user
With CDN → Indian CDN server serves Indian user
Result: Faster websites, Faster video streaming, better user experience
2. Reduces Load on Main Server: Instead of millions of users hitting one server, the traffic gets distributed across many CDN servers. This prevents: Server overload, Crashes during heavy traffic.
3. Better Performance During High Traffic: Websites like, Amazon, YouTube, Facebook use CDNs because millions of users access them simultaneously.
4. Protection Against DDoS Attacks: A CDN can absorb huge amounts of fake traffic and protect the original server. This improves security.
5. Improves Availability: So, websites remain online even during failures. If one CDN server fails, another nearby server can still deliver content.
Q) What is Cross Origin?
 The cross origin attribute in the script tag enables Cross Origin Resource Sharing (CORS) for loading external JavaScript files from different origin than the hosting web page. This allows the script to access resources from the server hosting the script, such as making HTTP requests or accessing data.
Q) What is {} denotes in react?
classes should come under {}. Whenever we are passing inside {}, will go as tag attributes of h1.
Q) What is difference between react.development.js and react.production.js files via CDN?
When you use React through a CDN, you usually get two versions: react.development.js, react.production.js (or react.production.min.js)
Both contain React, but they are made for different purposes.
1.	react.development.js: This version is used while developing your app.
Some features are:
•	Human-readable code
•	The file is not compressed, so developers can debug easily.
•	Gives warnings and error messages
•	React helps developers by showing detailed warnings.
But is has some drawbacks also:
•	Bigger file size, because it contains debugging tools and warnings.
•	 Slower than production version, extra checks make it slightly slower.
2. react.production.js: This version is used in real/live websites.
Some features are:
•	Optimized for speed. All unnecessary development checks are removed.
•	Smaller file size. The code is compressed/minified.
•	Faster performance. Better for real users.
It also has some drawbacks:
•	No detailed warning. React removes most developer helper messages.
•	Harder to debug. The code is compressed into very small unreadable lines.
So, while developing we can use develop.js to reduce bugs and later when the development is done and the app is ready to push to production we can replace the development link with production link.


