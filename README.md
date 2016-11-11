# CDS
Chrome DevSummit Notes

## KeyNote
> The state of Chrome and the Web Platform today, from the leader of the Chrome team.

Darin Fisher's (VP of Chrome Engineering) keynote:

* Mission: Move the web platform forward.
* Over 2 billion active Chrome users across mobile and desktop.
* Not just Chrome, the Web has a reach!
* Links the Web's superpower, physical beacons. [Polymon](https://polymon.polymer-project.org/)
* Every interaction step costs 20% of your potential users! 
* The Web is Mobile: Constrains has lead to innovation. 
* Build for Mobile Web is a priority: Connectivity constraints 
* Almost 60% in developing market are on 2G! 
* 230M in US, 460M in India (100M new users every year!) 760M in China.
* 65% of Indian population aren't online yet, 20% in US are not yet online. 
* Web works well really well in emerging markets: Flipkart, Voot Viacom18.
* Progressive Web Apps: Radically improving web experience. Not able on technology, it's more about new way of building web experience. 
* Demo on [cnet-tech-today](http://cnet.com/tech-today) a progressive webapp.
* Alibaba usecase study: 76% higher conversion due to progressive webapp; Singles day is an event in China on November 11th is the biggest event on the internet, 3 times more than cyber Monday, is on a progressive webapp.
* Fast - 53% of users abundant the site which takes more than 3 seconds to load. 
* Refresher on service worker API. 
* The Monica Per Test gets a mention. 
* Apps should be interactive within 5 seconds over 3G.
* Engaging - Add to Home screen; 4x more engagement due to this feature; prompting users sooner yields 48% more installs. 
* Install vs ATHS.
* Improving ATHS flow so the website will be in all apps location. 
* Ability to update the home screen icon or the name. 
* Push notification: 18 Billion push notifications sent everyday over 50,000 domains using it! 
* Seamless Sign-In: 85% reduction in sign in failure for AliExpress, Pinterest 10% increase in desktop logins. 
* WebPayments: Payment request API. 
* Productivity: Lighthouse, Real World condition testing, Security and Applications panel in Chrome. 
* Polymer gets a mention. 
* [Beta webcomponents](https://beta.webcomponents.org/) and AMP. 
* Predictability: The web should just work for developers. [browser-issue-tracker-search](https://browser-issue-tracker-search.appspot.com/)
* Looking ahead: Web assembly, WebGL 2.0, WebVR, WebAR, WebBluetooth. 

## Building Progressive Web apps.
> Thao Tran, talks about it.

* Looking back from the previous year to this in the progress of progressive webapp.
* Toys lasts for a week! Was the Flipkart PWA a unicorn, not really! 
* Beyond Flipkart the overall momentum went up. 
* 17K across 35 countries for a PWA summit. 
* What is a PWA? Radically improving web user experiences; It's a journey; 
* [building-indexable-progressive-web-apps](https://webmasters.googleblog.com/2016/11/building-indexable-progressive-web-apps.html)
* Housing.com Android App -> $3.75 and Mobile Web -> $0.07; 30% faster page load; 38% increase in conversion. 
* Early beta of [web elm](https://mobile-beta.westelm.com) PWA.
* Infobase Latin America: 65% of traffic is on mobile, < 1s page load time. 
* Lyft rolled out an mobile site just to test orders: they had 5x more rides from mobile web! So they are building a PWA which will be `<1MB` compared to 17MB andoird and 75MB ios.
* MakeMyTrip: Same day reservation from mobile web, PWA users book 3x more on their first visit! 
* The Weather company (An IBM Business): 18months ago they started: Moved to HTTPS, Web Push notification, 178 countries in 62 languages now!
* PWA: Acquistion; Engagement; Conversion; Retention.


## Sign-in on the web; Credential Management API
> Sabine and Eiji shared best practices for sign-in, and explains how the Credential Management API makes frictionless sign-in possible.

* Removing friction
* Growth: 54℅ will abandon rather than register.
* autocomplete inputs.
* Avoiding login friction: 92℅ leave the site if they can't recall the password.
* Leverage the power of the browser to make sign-up easier with credential management API.
* Session management and 2 cookie handoff using serviceworkers.
* Launched in Chrome 51.
* Problems that this API solves:  Auto sign-in, Smart lock for passwords.
* Auto sign-in across devices.
* Supports multiple accounts.
* Virtually enables a permanent
* Remembers federated accounts.
* Steps: Interrupt the from submission; send an Ajax request; store the credential information; update the UI.
* Federated login cases: Auth; store the identity information; store the credentials.

## Faster payments.
> One of the hardest web user experience challenges is enabling users to make payments. Zach shows us how with the new Web Payment API.


* Save the world from annoying checkouts form.
* PaymentRequest API: Not a new payment method; Not a gateway or a processor;
* Fundamentally build for users, is a standard-based API making payments easier for users.
* Main goals: Easy checkout and secure payment on Web.
* Supported data types: Credit cards and Android pay; Shipping address, options, phone, email, payer name.
* All the data points are stored and returned from the browser.

## Debugging The Web.
> Learn the state of the art in debugging using Chrome DevTools - all you need to know to expand your toolbox.

* Debugging like a boss: Making it clear on why there was an issue right on the devtools. In Chrome55+ the screen orientation will not affect the content much. 
* ES6 + DevTools.
* Text editor like REPL in DevTools.
* Better autocompletion on Objects.
* Substrings completions are better.
* Snippets....
* Place multiple inline break points in async or any line of code.
* Auto picks up the workspace mapping on drag and drop. (*Source maps)
* CSS coverage. Unuse CSS.
* NodeJS main context debugging in the same devTools.
* Application tab > manifest, clear storage, servicework et.al.
* Auditing PWA: Audit2.0 uses the power of Lighthouse. 

## Polymer, Web Components & You.
> Taylor Savage and Monica Dinculescu on the current state of Polymer, and how you can use Web Components to improve your development.

* Mobile device constraints. 
* Use the platform.
* Primay focus of Polymer are web-components. 
* Web Components V1. (Cross browser web component)
* Polymer 0.5 was an experiment, 1.0 was production-ready, 2.0 shall be web native.
* Who is using Polymer: Comcast, ING, BBVA, Netaporte, Coca-Cola, EA, Predix, Google and others. 
* Polymer App Toolbox: Set of web components, CLI, PRPL pattern; Example -> [shop](https://shop.polymer-project.org)
* JUMIA Travels use case: 75% of mobile connection is on 2G in Africa, >2x faster page load on 2G and 6x less data than native app.
* What's next on ploymer? Polymer2.0 - Web component V1 support; Better interoperability; Minimally breaking (backwards compatibility); Supports hybrid mode (i.e both on V1 and V2). 
* Polymer is light, it's just 12kb. 
* Polymer is about elements! element development is hard; Authors, maintainers and users of elements are the player here.
* 100+ elements in polymer; 3 orgs; 20+ apps; 500+ projects.
* Steps: Think of the features; Map the features to components; 



## Progressive Performance.
> Alex Russell on the important things to focus on in performance, and how to run great experiences on slow, inconsistent networks and low-power devices.

* [I realized I'd invented webpages](xkcd.com/1367)
* We are in the middle of a crisis. 
* RAIL: 100ms/8ms/50ms chunks/1000ms.
* 53% bounce with sites that take more than three seconds to load. 
* Collectively we are failing;
* Why are our tools slow?
* Your laptop is a filthy liar. 
* Understand the depth of the deficit. 
* The truth is in the trace. 
* Avg selling price of smart phones are going down; The next million users are buying their first phone.
* Motion Mark: Desktop version is like 25x times faster. 
* Power = Heat.
* A desktop can emit 60W of energy; Mobile devices can't do that!
* No thermal paste, no fans, no heat sinks on a mobile device. 
* Dark silicon and the end of multicore scaling paper. 
* 10.0Wh is all the battery got and it has to deal with GPU, CPU, NFC, Screen, Wifi et.al
* big.LITTLE arch. 
* "touch boost"; SMP vs HMP vs EAS. 
* Benchmarketing is A Thing! (Can't trust them)
* Mobile CPUs aren't really what think they are. 
* MLC Flash is how we make storage cheaper. 
* Read Perf: MBP: ~2GB/s and N5X: ~400MB/s.
* Mobile networks hate you! 
* Will LTE save us? Networks are slowing down. 
* Network overhead of one HTTP request! 
* Load less code, load it at the right time and let the browser help us whenever we can. 
* Ignorance / Privilege or both is the result of the frameworks today.
* Tools that doesn't use platform well, we end up in the Uncanny Valley. 
* Serviceworkers aren't just about offline experience it's also about reliable performance! 
* Mobile Hates You; Fight Back! 

## Real Talk about HTTPS
> Emily shows why the default for the web should be secure, and describes Chrome's mission to be honest with our users about HTTPS.

* What does HTTP mean for an avg user?
* HTTPS usage today: HTTPS at Google. (Transparency report); On Desktop platform 53% of users are using HTTPS sites; Not the pages but the % of time spent is important;
* HTTPS performance is getting better. Checkout [istlsfastyet](https://istlsfastyet.com) 
* Make HTTPS mandatory for privacy sensitive features.
* HTTP2 might also be adding an over head, but it's getting better.
* We need your help to get close to HTTPS everywhere!
* Don't be a Cry wolf victim.
* Chrome has funded to Let's encrypt.
* Ads that are only on HTTP not if they are Google sourced ads. 
* Enabling HTTPS webfundamentals.
* Search ranking should not drop, if you have done it right.
* DevTools security panel.
* The near future: In Chrome 56, there shall be a neutral information icon for HTTP pages with password or credit cards input in them.
* `#mark-non-secure-as` in `chrome://flags` 


## Planning for Performance: PRPL
> Sam explains how to get the browser to do things under budget - script and resource loading and more.

* The Pitch: Your manager asks: "Well does this work on mobile?"
* Mobile web is not more a subset of web, it's simply the web!
* Your users are not on the best phones.
* 19s is the avg load time on the mobile web! 
* User expects the page to load in 2s.
* What it takes to load a page? Request Page -> Request Assets -> Parse and Paint. 
* Network Delivery (for shop app): 
  * HTTP2 + no bundling on 3g => 5.5 seconds until first paint.
  * HTTP2 + no bundling + link rel="preload" on 3g => 3.3 seconds.
  * H2 server push + no bundling on 3g => 1.7 seconds.
* H2 server push is not cache aware, lacking resource prioritization, but H2 server push + SW is Nirvana! 
* Preload is good  for moving the start download time of an asset closer to initial request.
* H2 push is good for cutting out a full RTT.
* Nov 2010 -> 113kb of JS, today in 2106 we are shipping 400+kb of JS.
* V8 internal metrics in Canary. 
* Debugging a bundle. (Webpack)
* Webpack bundle analyzer. 
* Shipping less parsed code: `<script>` tag with invalid `type` or `<script>` tag with commented code i.e Angular lazy module loading, Polymer CLI, Webpack aggressive splitting plugin. 
* It's a mobile world: test on real devices and real network. (What your users would use.)
* Optimize network: sw, preload, push for fast first loads.
* JS parse has a cost: ship the smallest amount of JS possible.


## Predictability for the Web
> Rick and Robert explained how Chrome is improving predictability for developers, how we responsibly move the web platform forward, and how web developers can help improve the platform.

* The web has a problem: Working cross-browser is hard, inconsistency et.al
* Chrome, other web browsers and developers together can make it better!
* Fight the platform less! 
* Break websites less.
* A more coherent platform. 
* Remember when web development was hard?
* Cross-browser collaboration : Better interop, listening to web developers, the web is a commons.
* Blink Bugs: Closed more bugs than they have opened for the first time! 
* 300 bugs in September, 93% Triaged, 62% Resolved, 16% Fix landed.
* Out of top 1% of the stared bugs, 66% are fixed. 
* 15 % of the top 60 stared bugs were fixed this year.
* [wicg](https://github.com/wicg) Web Incubator CG.
* Consensus & Standardization across browsers.
* Experimental Web Plaform features flag.
* Minimizing breaking changes.
* An example of Bug 648589: Bug was reported on Aug, but got noticed on Sept and by Oct it was shipped.
* Breaking changes ain't just about regression it's also about deprecation. EX: GeolocationInSecureOrigin rejections.
* Great user experience vs composition of parts you can't control. [trade offs]
* Interventions: Minimally breaks existing behavior. EX: Throttled rendering. [WICG/interventions]
* Developer Feedback: Listening to devs, Understanding challenges, getting data.
* Improving Bug wizard for Chrome + Direct routing to the team who is working on the fix.
* Browser Bug Searcher within the [feedback](https://developers.chrome.com/web/feedback) page.

___

# Housing.com How We Built It?
> Housing.com show you their journey to creating a great user experience.

* With PWA:
  * 30% faster page load.
  * 10% longer avg session.
  * 40% lower bounce rate.
  * 38% conversions.
* Assets delivery: HTML streaming, Preload, Service Side Rendering.
* App Shell Model: Loding Screen of Purgatory. 
* With SSR first meaningful paint happend at 2.3s.
* Lazy Load & JS enabled interaction. 
* Coding spliting with webpack2.0
* JS and CSS sharding. 
* Route based chunks.
* Intent based chunks. 
* Example on the listing page: `notifyView.js` is around `32kb` unzipped, loads only when the interaction happens. 
* FMP `2.3s`, JS enabled inetraction `4.2s`.
* SW to precache: FMP `712ms` to JS enabled interaction ot `1.1s` 
* Credential Management API
* Maintenance: Label based github PR, Route based statistics.
* What next? React to Preact; `219` to `99`; AMP 


# Lyft How We Built It?
> Lyft's joureny. 

* Why we build a PWA? 
  * Greater reach.
  * Reduce friction.
  * Faster upload on experimentations. 

* Deep linking directly to PWA.
* No app approval, instant fixes.
* Nov -> Jul ->Planning, Aug -> Coding starts, Beta (React PWA), Oct -> Alpha (Angular MVP),
* Web payments, Service worker wait for push notifications on driver's arrival, which inturns has the payload for the ride, offline access, with background sync user can submit the feedback without bothering about the connection. 
* Putting JS on diet: Lesser deps, Tree shaking, Type aware Minfication. 
* React, Webpack, TypeScript: Bundle size is `40kb` gziped. 
* Challenges: Bleeding edge tech; Limitations with other platforms. 
* Don't animate opacity! 
* #Weekly rides when up by 5x.
* Wrapper app around Amazon app. 
* Next: Pove & Optimzie conversion funnels, Experiment and more features! 

# From AMP to PWA - the best of both worlds
> Paul Bakaus explains the opportunity in AMP, and how to build great Progressive Web Apps with AMP.

* 53% will drop off if the first load takes `3s`
* 200-300ms latency with mobile bandwidth. 
* RAIL says load under `1s`.
* Current situation: Avg Mobile page loads in `19s` with `77%` of them take `10+s` with `214` requets.
* First impression, first click is what matters. 
* AMP: CMS -> AMP-HTML -> Speed up by AMP cache -> Fast loading -> Across platforms. 
* Build portable beautiful high-performance webapps. 
* AMP cache: Pre-renders only the first viewport, No 3rd part JS, One less privacy issue. 
* AMP pages and AMP open-source JS library.
* AMP constraints: NO {JS, SW, PushNotification, WebMainfest} from AMP cache. 
* AMP: Instant delivery and optimized discovery.
* AMP to PWA: AMP UP and AMP DOWN.
* AMP is not just an website, it's an ultra portable content unit and a data format! 
* One window, one instance of AMP lib and multiple documents. 
* PWA: XHR -> Shadow Root -> Shadow Dom -> DOM.
* Coming up: Shadow slots.
* One AMP, One PWA, One Request.
* Fallback URL rewriting: If we reach AMP page from an non-SW browser, it can be detected. 
* Wallmart: 3 engineers for 2 weeks, Reusing exisiting AMP rendering, pipeline unchnaged; Resulted in: Performance, UX improvements, Prefeting the cache, web push.
* Pain Points (from Wallmart): 0
* PWAMP: for sites with static content.

## Production PWAs with frameworks
> Addy works through building Progressive Web Apps with React at scale. Featuring special guests, Flipkart, dive into the performance and loading patterns needed to make frameworks competitive on mobile.

* Polymer has been a tesla! (the car)
* Frameworks can be fast if we put the work in.
* Flipkart: Time to interactive -> `4.2s`
* Housing: Time to interactive -> `4.8s` 
* Navigation begins ->  First Paint -> First Contentful Paint -> First Meaningful paint.
* Lighthouse with remote debugging is worth trying. 
* Addy's survey:
  * `83%` of them use webpack.
  * `58%` thought they were using webpack, but webpack community says it would be `10%`.
  * `11%` SW, `14%` HTTP2 and `19` tree shaking.
  *  Avg react app in the survey `12s` on `3G`.
* Try not to keep the main thread busy.
* `1MB` script (250KN minified) JS parse, compile and eval -> `3s`. 
* Test on real devices!
* Less code loaded better helps everyone. 
* Code splitting and async loading.
* Bundle loader calls require.ensure for you.
* Code-Splitting with react-rotuer. 
* PRPL pattern with webpack.
* HTTP/2 with the AggressiveSplittingPlugin.
* Code splitting itself is not a panacea: `9.8s` TTI average. 
* Ask yourself: What's in your bundle?
* RFC: Webpack Performance Budgets.
* Preact: `3KB` alternative to React with same ES6 API.
* Source map explorer. 
* preact and preact-compact is worth checking.
* Housing: 1st visit on 3g in `3.5s` and repate visit is `0.8s`.
* APP Shell: SWPrecacheWebpackPlugin.
* Support all target users using progressive enhacnement.
* Universal JS has issues: 
  * Get stuck in uncanny valley.
  * `renderToString()` impacts TTFB.
  * `renderToString()` can monoploize CPU.
* Mobile -> Desktop Flipkart:
  * React, react-router, webpack, redux, node, express.
  * Route based code splitting.
  * PRPL
  * Partial SSR.
  * SW.
* Flipkart Mobile: Build-time rendering; App Shells; SW; Composition of multiple SPA.
* Flipkart Desktop: Partial SSR, No app shells, Chunked reponse for the first request allowing faster TTFP, SW used for caching data and resources. 
* Chunking, Streaming and code splitting.
* First paint of Flipkart: Search box, without JS. 
* Major wins for Flipkart:
  * Route based code-splitting.
  * Smart preloading.
  * Chunked encoding.
* Impact of the Flipkart migration: 
  * 2x conversion.
  * Reduced bounce rate.
  * 50% time reduction 
  * 50% increase in number of pages crawled.
  * DevOps 70% reduction in the effort.
* Gotchas:
  * CORS in webpack & route-based code-splitting.
  * Cache-invalidation & webpack manifest.


## May We Help You? Tools and Libraries for Progressive Web Apps
> Jeff Posnick walks through Lighthouse and all the tools and libraries we produce to help web developers easily build great Progressive Web Apps.

* Copy & Paste SW? Careful about pitfalls on cache {version, URLs}, fetch handlers, clearining SW. 

* Production ready SW, checklist: 
  * Use an Asset Manifest. (build time)
  * Smart updates. (hash change)
  * Runtime cleanup. (LRU expiration cache)

* Tools for production ready SW:
  * sw-precache.
  * sw-toolbox.
  * web starter kit.
  * Polymer starter kit.
  * sw-precache-webpack-plugin.
  * sw-offline-google-analytics.
  * lighthouse.

* What a modren SW framework would look like?
  * ES2015 modules and syntax throughout.
  * Feature parity with exisiting libs.
  * Routing + Runtime handlers + Request behaviours. 

## Client storage: shave seconds off your load time with one simple trick
> Dru explores the landscape of storage APIs: past, present and future, provides best practices and explains the finer details.

* 2.5% of page traffic uses indexDB or cache storage. 
* Client storage is the largest loading performance win.
* 53% of users quit the site if it takes more than 3s to load the page.
* On 3g 320s to load 1MB! 
* Offline vs Cache: Think of storage of a cache. 
* Cache: Browser cache, Optimized browser cache, Content caching, Full cache control.
* Browser cache: 
  * Speed up repeat visit.
  * Network responses only.
  * Unpridictiable.
  * No granularity.

* Optimized browser cache:
  * Minimal practive page load.
  * Network responses only.
  * Unpridictiable.
  * No granularity.

* Content caching:
  * Proactive page load improvements.
  * All response types.
  * Some predictability.
  * Content granularity for content only.

* Full cache control:
  * Proactive page load improvements.
  * All response types.
  * Fully predictability.
  * Content granularity for content and network request.
  * Offline support.

* Best practices:
  * Client side chunking.
  * Preload pages the user might visit.
  * Save commonly repeated components.

* Libs:
  * idb
  * localForage
  * others...

* Browser quota limit
  * Chrome - 6% LRU when full.
  * Firefox - 10% LRU when disk is full.
  * Safari - at least 10% dosn't clear.
  * Edge - hmm doesn't clear.

* Things to note, when you think about storage:
  * Overall storage footprint.
  * Read : Write ratio.
  * Time since last eviction when you store something. 

* Persistent storage:
  * Chrome 55, in development in FF.
  * Granting heuristic.
  * Show offline UI once you get the permission
  * Use the quota estimate API to mesaure usage.

* Upcoming: IDB Observers; Async Cookies; IDB Promises; Writeable Files.

* Takeawaus:
  * Storage isn't just offline.
  * `50MB` is min storage for now.
  * IndexDB is for the strcutred data and cache for the other.

P.S: I am jet-lagged forgive the typos, shall fix them sooner.
