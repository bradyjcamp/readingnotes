# Express

## Introduction to Node

- [Node](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction) is an open-source runtime environment that allos devs to create server side apps in JS.
  - Offers NPM to install a large number of packages.
  - Node is also very dynamics and flexible and can be used on pretty much any OS.

## Introduction to Express

- **Express** is a Node *framework*.
  - Allows us to write different requests to different URL routes with HTTP verbs.
  - There is also a large of amount of express middleware such as **cors** or **morgan**(which is a logger middleware) that can be installed.

## NPM

- NPM stands for [*node package manager*](https://docs.npmjs.com/about-npm).
  - It is used to install different libraries, packages, and frameworks to your Node application.

## TDD

- **TDD** stands for *test driven development*
- It is a process used in programming to test a single feature of code to ensure it is working.
- It will essentially increase the time it takes to create an application initially by adding tests, but will decrease the amount of bugs and time it takes a team to go through an app and debug.
- It is important to remember to not:
  - forget to run tests frequently
  - write too many tests at once
  - write single large tests
    - [TDD](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1))

## CI/CD

- Continuous Integration / Continuous Delivery
  - When there are multiple devs working on the same project there will be a large amount of different branches made off of the same master branch.
  - **CI** helps to make sure all changes integrate smoothly by catching all bugs and reducing merge conflicts.
    - This is what we see in GitHub when it is checking merge compatibility.
  - **CD** this means that the code is developed to release at any time.
    - GitHub tracks and communicates with other systems when changes are made to make this a smooth process.
- [Professional Guides: Continuous Integration Continuous Delivery](https://www.youtube.com/watch?v=xSv_m3KhUO8)
