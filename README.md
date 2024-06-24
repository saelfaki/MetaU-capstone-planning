Project Plan
[Project Name]
Intern: Saja Elfaki
Intern Manager: Chady Ben Hamida
Intern Director: Josh Katz
Peer(s): Ning Lyu, Hanlu Chen

Overview
Category: Education
Story: A networking website connecting low-income high school students seeking scholarships profiles with scholarship benefactors willing to support their education financially. They can follow each other and see each other's posts.
Market: This app is aimed at high school students from low-income backgrounds who need financial support for college, as well as older adults (scholarship benefactors) who are interested in contributing to these students' education.
Habit: The app would be used frequently by students to search for scholarships and connect with mentors. Benefactors would use it periodically to search for students to support, review applications, and receive updates on their supported students.
Scope: The initial scope for this project is text posts from both students and beneficiaries to network. 

Product Spec

User Stories

Required
Users (both students and benefactors) can securely log in to access their accounts.
New users can create an account.
User can create / edit / delete posts: 
Students: Can create posts seeking advice on scholarships, share their achievements, and update on their academic journey.
Benefactors: Can create posts about available scholarships, success stories of supported students, and updates on their donations.
User can view a feed of posts
Users can connect with mentors (for students) or potential recipients (for benefactors) by adding them as friends to stay updated on their activities and posts. Also able to remove each other. 
User can like posts
Users can see their profile, which includes their bio and past posts.

Optional
User can create multi-media (photos, videos) posts
User can see notifications of actions made by their friends
User can edit their profile information
User can see their friends’ profile
User can comment on posts
User passwords are encrypted in the database for security
Screen Archetypes



Data Model
[Describe the data you’re going to need to back your application. This can include database models (like tables), or external data you’ll require from some API.]

Profile Attributes: 
id (integer)
username (text)
password(text)
email (text)
bio (text)
role (text: student or benefactor)

Post Attributes:
id (integer)
user_id (integer - foreign key to User)
content (text)
Interview location (text, optional)
created_at (datetime)
updated_at (datetime)

Friends Attributes:
id (integer)
user_id (integer - foreign key to User)
friend_id (integer - foreign key to User)(user who is being added as a friend)
created_at (datetime)

Like Attributes:
id (integer)
 user_id (integer - foreign key to User)
post_id (integer - foreign key to Post)
created_at (datetime)

Server Endpoints
[Describe the endpoints that your application is going to consume from your server. If you’re using REST, then you’ll probably want to include the method (GET/POST/etc) and the expected parameters (query parameters, body parameters, etc.)]

GET/posts: Fetches a feed of posts from friends and followed users.

POST/posts: Creates a new post.

PUT/posts/{post_id}: Updates an existing post.

DELETE/posts/{post_id}: Deletes a specific post

POST/friends/{user_id}: Adds a user as a friend.

DELETE/friends/{user_id}: Removes a user from friends list.

POST/posts/{post_id}/like: Likes a specific post.

GET/profile: Retrieves the user's profile information.

POST/profile: Creates a new user account.

PUT/profile: Updates a user's account.
Navigation

Login/Registration Screen: Allows users to log in or register for a new account.
Home Feed Screen: shows a feed of posts

Create Post Screen: allows users to create a new post, text box and post button

User Profile Screen: displays the user's profile information, username, bio, posts by user, edit post button, edit profile button

Friend List Sidebar: list of friends username, unfriend button

Search Friends Screen: allows users to search for and add new friends, search bar, list of search results, add friend button

Project Requirements
[Based on the Project Guide, describe how your project is going to be fulfilling each of the base project requirements.]

Technical Challenges
For your project, you should demonstrate that you can apply what you’ve learned so far and expand on that knowledge to write code and implement features that go beyond the scope of the projects you worked on during CodePath.

Based on the general idea and direction of your project requirements, your intern manager will create at least two (2) Technical Challenges for you. This section is all about explaining what they are and how you’re planning to tackle them - you’ll work together with your manager to fill it out. 

Technical Challenge #1 - [Name/Small Description]
Matching system with hs students and benefactors 
What
What problem are you solving, and what parts go beyond what you learned in CodePath? 
How
Explain in words how you’ll solve this problem. 

You’re encouraged to expand on this section with pseudo-code, links to external frameworks, architecture / design diagrams, anything that you can use to explain this to others!
Technical Challenge #2
Calender when deadlines are approaching for students when matched
 uploading secure documents in application process
What
How

Database Integration
[Describe what you are using for database storage. For example, Parse, MongoDB, Sequelize, etc.]

PostgreSQL database
External APIs
[Describe at least one external API you’re using for your project. For example, Google Maps, Spoonacular, OpenWeather, etc.]

Google Maps, photo of interview spot

Authentication
[Describe how user authentication is handled for your project, including logging in and signing up. Also describe any kind of cookie / session management you’re doing and how you’re implementing it, and how this affects navigation between different screens by the same user.]

Visuals and Interactions
[Provide details on how your app is fulfilling the following UI craft requirements, and how these are technically accomplished.]

Interesting Cursor Interaction
UI Component with Custom Visual Styling
Loading State

