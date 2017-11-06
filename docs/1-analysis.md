# Analysis

## Table of Contents
- [The Idea](#the-idea)
  - [A Reddit Alterative](#a-reddit-alternative)
  - [A Self Governing Democracy](#a-self-governing-democracy)
  - [An Open Platform](#an-open-platform)
  - [A Modern and Minimalist Experience](#a-modern-and-minimalist-experience)
- [The Investigation](#the-investigation)
  - [Interviews](#interviews)
  - [The End User (Stakeholders)](#the-end-user-stakeholders)
  - [The Focus Group](#the-focus-group)
  - [Research into Existing Systems](#research-into-existing-systems)
- [The Analysis](#the-analysis)
  - [Essential Features](#essential-features)
  - [Computational Methods Required](#computational-methods-required)
  - [Success Criteria](#success-criteria)
  - [Limitations of the Project](#limitations-of-the-project)
  - [Hardware and Software Requirements](#hardware-and-software-requirements)

## The Idea
### A Reddit Alternative
If you do not already know what [Reddit](https://www.reddit.com/) is, this section will explain the basic premise behind it. 
Reddit was founded in 2005, and has largely remained the same since its inception. 

As Wikipedia puts it (paraphrased): 
> Reddit is a **social news aggregation**, **web content rating** and **discussion** website. 
>   
> Reddit's registered community members can submit content such as text posts or links. 
> Registered users can then vote submissions up or down that determines their position on the page. 
> Submissions with the most up-votes appear on the front page or the top of a category. 
> Content entries are organized by areas of interest called "subreddits".

Corum will borrow these basic ideas. 
The reason I wanted to create Corum, instead of continuing to use Reddit, is explained in the following subsections.

### A Self Governing Democracy
Being self governed means that those that are being governed, govern themselves and each other. 
There is no higher authority that makes decisions. 
In the case of a forum site, this means that it is solely up to the users of the forum as a collective to decide what content belongs on it. 
Corum will be designed and developed from the ground up to strictly follow this principle.

Users will be given one vote each on every post, and each vote will be treated equally. 
Up until now, this sounds very similar to [Reddit](https://www.reddit.com/). 
The way that Corum differentiates itself from existing solutions like Reddit is by making the vote that users are given actually mean something. 
If users generally vote positively on a post, then the post will remain. 
However, if a post gets a mostly negative response, it will be automatically removed from the sub forum that it was posted in. 
This means that if someone posts something that doesn't belong on the forum, it will be removed by the users themselves _fairly_. 
This is instead of having a moderator remove it based on their own opinion of the post, which could be biased.

The idea of having self governing forum software means that the role of the forum moderator no longer needs to exist.

This is a good thing because:
* It means that the forum requires less maintenance. (Less man power required)
* The users of the forum are responsible for maintaining it. (More **neutral** and **fair**)
* The removal of the moderator role keeps code complexity down. (Only one type of user account needs to exist, and no 'admin control panel' is required)

### An Open Platform
While it is one thing to keep the platform itself democratic, it is also important that the management and development is kept democratic as well.
As of 1st September 2017, after many years of being open source, [Reddit has decided to stop developing in the open](https://www.reddit.com/r/programming/comments/6xh3xp/reddits_main_code_is_no_longer_opensource).
As an advocate for open source, I believe that Reddit has made the wrong decision here. 

Being open source means that anyone who wants to contribute can. 
They can easily propose new features, report and/or fix bugs, and freely read the source code knowing that anyone else can too. 
Developers cannot go hiding things in the source code like unnecessary tracking etc. 
Every decision made by the project is made by the users.

This means that ultimately, the users of the forum decide the direction that Corum takes in _all_ aspects.

### A Modern and Minimalist Experience
As mentioned [above](#a-reddit-alternative), Reddit has not changed how it looks or feels very much at all since it was created in 2005.
However, the reasoning behind this decision is probably that they do not want to make it feel unfamiliar for returning users.
For Corum, this means that I can completely rethink the way a forum should look, feel and function, as it is a new project.
With that being said, it is important that the transition from Reddit to Corum is as easy as possible for new users.
So, if I keep the basic features of Reddit intact and keep the UI & UX simple, new users should be able to get up and running with Corum quickly. 

## The Investigation
### Interviews
I will be interviewing people that I know are users of Reddit to get an idea of what they like and don't like about Reddit.
This will help me understand what features I should borrow, leave out, as well those that could be added that don't currently exist.

#### Questions
1. What do you like about it?
1. What don't you like about it?
1. What do you use regularly on it?
1. What do you not use on it?
1. What would like to see in the future on it? 

#### Answers

##### Interviewee 1
1. > I like the post voting system and how popular articles raise to the top of each sub-reddit
1. > I don't like the look of it. I don't think it looks very modern.
1. > When browsing a sub-reddit and see a post I like, I almost always look what site the link is from.
1. > I never look at the name of the author of the post on the main sub-reddit.
1. > I would like a more fluid experience using it. I want it to feel like im using an app.

##### Interviewee 2
1. > The fact that I can see instantly how popular a post is, which isn't a feature of many forum websites.
1. > I don't like that a sub-reddit can choose what it looks like, I find it very jarring to my experience when switching to a sub-reddit that looks totally different than the last.
1. > I use the navigation bar at the top a lot as I am always moving between sub-forums
1. > I never really look at the information that is on the right side of every sub-forum, I only go to a sub-forum to look at what new has been posted.
1. > I post quite a lot, so it would be nice if the interface of creating a new post was simpler.

##### Interviewee 3
1. > I like that I can subscribe to particular sub-forums and have them easily accessible. 
1. > I think that there is too much information about each post of sub-forums main pages. (time posted etc.)
1. > I use the sort functionality quite a lot to see whats new, but also what is popular.
1. > I don't really look at or care about the number of people that are current online on a sub-reddit. I would rather a cleaner interface.
1. > I would like to see a major redesign of the whole site, it doesn't feel modern at all anymore.

##### Interviewee 4
1. > I like that other people can comment on posts, with their own opinions.
1. > I don't like the fact that moderators can remove whatever they please.
1. > The comment section on each post, it often is of similar value to the actual post.
1. > I think the profile preference section is way too complicated, and it doesn't need to be.
1. > For Reddit to open source their code again, I don't like the fact that I cannot see the source code of software I use regularly.

#### Insights Gained from these Interviews
As a summary from these interview responses, I can tell the following:

- People like how the Reddit voting system works
- People want a more modern version of Reddit (Like a web app)
- People dont like how cluttered Reddit's UI is
- People like the idea of Reddit, but think it could be executed better

I will take these interviews responses into account when designing and developing Corum.

### The End User (Stakeholders)
In the case of a forum like Reddit, as evident from the [above interviews](#interviews), the end user / audience of a project like this can be wide.
For example, on Reddit, there are sub forums ranging from politics to comedy to programming.
This also means that the potential target audience is large, as anyone that wants to visit the site to read or engage in discussion can.

As Corum aims to be similar to Reddit, it will likely foster the same type of content on it.
Unlike forums that are designed for a single topic or purpose, Reddit, and therefore Corum, is designed to have anything on it.
This means that whatever people want to talk about on it, then can. (This could be sharing news, collaborating on research, or just chatting to each other.)

The reason why an end user would use Corum over a site such as Reddit could be for many reasons.
For example, it could be that they like the democratic system of moderation as discussed, or that they prefer the modern experience that Corum will provide.

Also, there are two different types of users that could use Corum; the users that regularly visit and actively engage in discussion, and the users that will only ever visit the site when directed from a search engine. 
In the following sub sections, I will outline what Corum should do to try and cater to the needs of these two types of users.

#### Users That Have Different Interests
Users of the site will have different interests, which means that Corum needs to work well for all, and the site should not be designed for only one type of content. 
**Good computer literacy should not be a given**, so the interface should be layed out in a simple manner. 
Colour should also be kept to a minimum to keep the site looking neutral.

#### Users That Use the Forum Differently
For users that have never visited or rarely visit the site, the UI (User Interface) and UX (User Experience) shouldn't be surprising so that this type of user can get whatever information they are looking for quickly and efficiently.
Also, the site should work equally as well for returning, regular users. 
This means that the site should keep a similar structure and look throughout, and should not get in the way of the user.

### The Focus Group
The focus group will consist of people I know that regularly use sites such as reddit, and of those that only use such sites for information gathering. 
This means that the focus group will contains the two possible types of end users as mentioned in the previous section. I will use this group for testing and feedback on Corum as it develops.
The group will contains people of a wide age range, to most accurately represent the end users, as Corum is not aimed at any particular age group.

### Research into Existing Systems
#### [Reddit](https://reddit.com) (Proprietary [as of September 2017](#being-open))

![Reddit Front Page](https://raw.githubusercontent.com/joealden/corum/master/docs/images/reddit.png)

**Reddit** is a very popular forum site that is home to a wide range of topics, where people can post links to other websites, or just have discussions actually on the site. 
Users can up-vote or down-vote posts if they like or dislike them. 
This is where the inspiration of Corum came from, however I thought that the vote that the user is given on each post could be given more value.

As a regular reddit user, I have had plenty of time to get a grasp of its features and what it feels like to use.
As Reddit is a major inspiration for this project, a lot of its features will be borrowed.
This is on purpose, as the target audience of Corum will be mainly those who have already had experience with Reddit.
This will mean that it will feel familiar and it will be easy to get started.

While the idea of Reddit is quite simple, in my opinion, and others (as shown by the [interviews](#interviews) with fellow Reddit users), the user interface is cluttered, with many features that are rarely used such as the amount of people online etc. 
Corum will strive to be a simpler version of Reddit.

#### [Hacker News](https://news.ycombinator.com/) (Proprietary)

![Hacker News Front Page](https://raw.githubusercontent.com/joealden/corum/master/docs/images/hackernews.png)

**Hacker News** is a similar site to Reddit, however it is a lot simpler.
There are no sub-forums, as it is a site dedicated only for computer science related topics such as programming.
The user interface is very simple (and quite dated in my opinion), which means that it doesn't get in the users way. However, I believe that it is too simple, and too niche (As it is only for programmers).

I believe that there is space in the forum software landscape for a site that is simpler than Reddit, but one with more features than Hacker News. This is where Corum could fit in.

#### [phpBB](https://www.phpbb.com/) (Open source)

![Solus' Forum Front Page](https://raw.githubusercontent.com/joealden/corum/master/docs/images/solusforum.png)

**phpBB** has different goals than Corum, Reddit and Hacker News. 
Instead of being designed to run from one website, it is designed to be used by anyone who wants to setup their own forum.
An example of where phpBB is deployed is at [Solus' Forum](https://solus-project.com/forums/). 
This can be seen when looking at the pages footer. 

phpBB can be themed so that it can fit the style of any website it is being run on. 
This means that the look or layout of phpBB isn't really an issue as it can be easily altered. 
However, as Corum will be a more similar project to Reddit, Corum does not need this extra complexity of being able to change its looks. 
I like the simplicity of Solus' forum theme, and Corum will take some inspiration from its looks.

## The Analysis
### Essential Features
From my research into existing systems, as well as the interviews I have done, I believe this to be a good set of basic features that Corum needs.

#### Page Layout
- Header (Top of the page)
  - Top left - Logo linking to homepage
  - Top Right - Login/logout/sign-up button/link
- Navigation (Left side under Header, think this is better placement than Reddit at the top as it is easier to navigate through)
  - Sub-forum subscriptions at the top (Called Favorites, users can access their favorites first. This will mean that returning users can access content they want to see quicker)
  - All other sub-forums below (Search bar of all sub-forums for easier navigation around the site)
  - Highlight the currently selected sub-forum in the nav (So the user can easily see where they are)
- Current sub-forum (Render selection message upon first load/after login when no sub-forum is selected - gives first time user some helpful instructions on what to do)
  - Give user sort selection (newest / most popular [This gives the user a choice on how they wish to view the content])
  - Eventually make it so posts are loaded in dynamically (paginated)
  - Each post
    - Current amount of up votes (Shows popularity of post, which could be an indication of how good the post is and if it is worth viewing)
    - Title -> links to link/post
- Selected post (Fills the space where the sub-forum was)
  - Title (So that the user can always see where they are)
  - Time Posted (This can give context of how relevant the content is [For example, an older post may not be so up to date])
  - User that posted it (Could tell the user if the information is credible)
  - Amount of votes
  - Content
  - Comments (For discussion of the post, show message if empty)

#### General Features
- Login System
  - Account Creation / Sign-up (username, password)
  - Require login to post/comment (So that other users know who posted / said what)
- Self governing voting system
  - Each user gets a single vote (up or down) for each post (like Reddit)
  - Posts with positive votes rise to the top (popularity sort)
  - Posts with negative votes go to the bottom (popularity sort)
  - Posts that get -25 (due to change) 'votes' are removed from the sub-forum
    - This point is the key to the self governing system, as the features before it are borrowed from Reddit.
    - Theoretically, no matter how popular the sub-forum is, if more people like the post that don't, the post will remain. 
    - If more people dislike a post than like it (within the vote threshold) then it will be removed automatically.
    - This means, that instead of a moderator moderating the sub-forum, the users do it themselves. This comes back to the point for neutrality and fairness, as the sub-forum community as a whole gets to decide what is allowed on the sub-forum.
- API
  - Use GraphQL
  - Setup the backend on graphcool

### Computational Methods Required
Here is a list of computational methods that could be used to create Corum, as well as how they will be useful.

#### Decomposition
By using [Vue](https://vuejs.org/), I will be able to break the UI down into small, reusable components. 
This allows developers to create large projects while keeping it manageable and maintainable.
In the case of Corum, it would not be manageable or maintainable to create the whole site in one large file.
Not only would it be a nightmare to work on, common code and components could not be reused across different pages.

#### Abstraction
Also with the aid of [Vue](https://vuejs.org/), I will be able to compose large components from multiple smaller components.
This means that the complexity of each component can be abstracted away when taking a high level view of the composite components.
For example, each page of the site will be considered its own component, but it will contain many smaller components such as the navigation component and a main content component.

#### Pattern matching
I will attempt to implement search functionality into the navigation part of the application, this will require pattern matching. 
Also, as this project will make use of client-side routing with [vue-router](https://nuxtjs.org/api/components-nuxt-link), pattern matching is required to direct the user to the correct page.
For example, navigating to `/subforum/:subforum` will render the subforum page component with the data from the path variable `:subforum`

#### Sorting and searching
Related to the method above, searching will be used as the subforum navigation will be searchable.
This will most likely be achieved by using a regex (Regular expression), or a composition of built in javascript string methods.
Sorting will also be used, as the user will be able to select the order in which they see posts in the sub-forum.
This will most likely be handled on the server side, as in the end, I will want the subforum post list to be paginated. 
This means that a sort would require a re-fetch from the server, as the client will not have all the data at once.
Graphcool provides a 'orderBy' parameter in their queries, so it will not be too complex to implement. 

#### Use of Multiple Programming Paradigms
##### Declarative
Vue allow me to develop components as [SFCs (Single File Components)](https://vuejs.org/v2/guide/single-file-components.html)
This allows me to create my components declaratively and encapsulated, as the HTML, JavaScript and CSS for that particular component will all be contained within the single file.
Also, as I am using Vue, I do not have to worry about _how_ my components will get rendered to the [DOM (Document Object Model)](https://en.wikipedia.org/wiki/Document_Object_Model), I just tell Vue _what_ I want to render, and Vue will figure out the most efficient way to do so.

##### Functional
Programming in a functional style helps improve code maintainability, readability, and [more](https://en.wikipedia.org/wiki/Functional_programming).
Also, the project will be easier to test (Due to things such as pure functions not having side effects, and function composition allows for better testing in isolation [Unit testing])

JavaScript provides great tools to build software in a functional paradigm, this includes features such as:

- [First-class Functions](https://en.wikipedia.org/wiki/First-class_function) - This means that JavaScript treats functions the same as any other variable. Functions can be passed as arguments to functions, returned from functions, assigned to variables and stored in objects and arrays.
- [Arrow Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) - Allows for concise function declarations and clean [function currying](https://en.wikipedia.org/wiki/Currying). For example:

```javascript
// Regular function expression - not curried
const concatRegular = function(string1, string2) {
  return `${string1} ${string2}`;
}
const joinedTextRegular = concatRegular("Hello,", "world!"); // "Hello, world!"

// Arrow function expression - curried
const concatArrow = string1 => string2 => `${string1} ${string2}`;
const joinedTextArrow = concatArrow("Hello")("world!"); // "Hello, world!"
```

- Functional Array Methods 
  - [`Array.prototype.map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
  - [`Array.prototype.filter`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
  - [`Array.prototype.reduce`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)
- Immutability 
  - [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) 
(Not perfect, reference only so objects + arrays can be mutated, use 
  - [`Object.freeze`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/freeze) 
(for both objects and arrays) or something like [Immutable.js](http://facebook.github.io/immutable-js/))

#### Real Time Data Processing
I will implement real time search functionality for the navigation, as well as possibly real time sub-forum updates like updating the current amount of votes updates without a page refresh. 
This will be achieved through the use of [GraphQL Subscriptions](https://www.howtographql.com/vue-apollo/8-subscriptions/).

### Success Criteria
- The UI should resemble the layout seen in the [GUI Design section](#gui-design)
- Users can click on subforums, and the site displays the subforum's posts.
- Users can click on posts, and the site displays the content of the post.
- Users can click on the `signup` button and signup to the site (Details saved to backend)
- Users can click on the `login` / `logout` button and login to / logout of the site (Check details against the backend)
- Logged in users can add & remove subforums to their `favorites`
- Logged in users can vote on posts
- Logged in users can comment on posts
- Logged in users can create new posts

### Limitations of the Project
#### Account Recovery 
If the user losses their email / password, they will not be able to recover it. I am deciding not to include this feature, as this version of Corum is only a prototype, and the creation of this feature is not essential, and it would take quite a lot of time to get working.

#### Creation of new sub-forums
Unless I have time near the end of the project, I will not be implementing the ability to add new sub forums. This can still be done manually by the owner of the site, so it is not an essential feature to implement just yet.

#### Responsive CSS 
Having responsive CSS would mean that the site would look good on both desktop and mobile devices. As mentioned, this is just a prototype version of the site, and as it is only a visual problem, it would be unwise to spend a lot of time making it look good on mobile devices.

### Hardware and Software Requirements
In the following subsections, I will explain both how to host and view the site. 
These two use cases will require different software and hardware.

#### Hosting the Site
The project is based on a full JavaScript stack, so it is able to be developed and deployed on any OS that Node.js supports.
If you haven't already, download Node Version 8+ [here](https://nodejs.org/en/download/current/) and install it. This will give access to Node and NPM (Node Package Manager).
Now your system is ready to develop and / or deploy Corum.

To get a copy of Corum on your local machine, clone this repo using the following command ([Git](https://git-scm.com/) must be installed):
```bash
git clone https://github.com/joealden/corum.git
```

##### Development
[Nuxt](https://nuxtjs.org/) provides a pre-configured hot reloading dev server (Using webpack-dev-server under the hood), which means I can save a file and see the resulting change instantly in my browser.
This dev server also provides an in-browser error overlay, which allows for easier debugging.

To start the dev server, run the following commands:

```bash
npm install
npm run dev
```
To view the site, navigate to `http://localhost:3000` in your browser.

##### Deployment
To start the production server, run the following commands:

```bash
npm install
npm run deploy
```

#### Viewing the Site
##### Hardware
As mentioned in the section talking about the projects limitations, Corum will be actively made compatible with mobile devices (Such as tablets and smartphones), as it is currently only a prototype version. In the future, Corum could be made to work on mobile devices as well. For this reason, it is recommended that Corum is viewed on a desktop or laptop.

##### Software
As Corum is a website, any modern browser on any modern Operating System will work.
As I am using reasonably new features such as [CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout), it is recommended to view the site on the most up to date versions of Chrome, Opera, Firefox or Edge. The reason I have chosen not to support older browsers is because it would make the user experience of those using modern browsers worse, as well as making it a lot harder to develop.  

#### Other Software Information about the Project

##### Corum's Backend
I am planning to use [graphcool](https://www.graph.cool/) as my API and user authentication backend.
Graphcool is a BaaS (Backend as a service) that combines 'serverless' (A service like AWS Lambda) and GraphQL (An API query language).

This will allow me to easily develop the client side of the application without needing to worry about the implementation details of the GraphQL backend that it fetches data from. 
Graphcool is a free to use service for small sites, as shown [here](https://www.graph.cool/pricing/).

##### Libraries / Tools To Be used
**ALL** of the code and technologies that will be used for this project are open source.

- **Language** - [ES2015](http://es6-features.org) + [ES2017](http://node.green/#ES2017) (JavaScript)
- **Runtime for development** - [Node.js 8.x.x](https://nodejs.org) and [Chrome](https://www.google.com/chrome/browser/desktop/index.html)
- **VCS ([Version Control System](https://en.wikipedia.org/wiki/Version_control))** - [Git](https://git-scm.com/) with [Github](https://github.com/joealden/corum)
- **Package Manager** - [NPM 5](https://npmjs.com)
- **Task Runner** - [NPM Scripts](https://docs.npmjs.com/misc/scripts)
- **Framework** - [nuxt](https://nuxtjs.org/)
- **View** - [Vue](https://vuejs.org/)
- **Data Fetching (GraphQL)** - [Apollo Client](https://github.com/Akryum/vue-apollo)
- **Client-side Routing** - [nuxt-link (vue-router)](https://nuxtjs.org/api/components-nuxt-link)
- **Module Bundler** - [webpack](https://webpack.js.org/)
- **JS Compiler** - [babel](https://babeljs.io/)
- **JS Linter** - [ESLint](https://eslint.org/)
- **Testing** - [Mocha](http://mochajs.org/)