---
title: writing a theme rendering framework
date: 2015-04-04
writing: true
published: true
---


While working at Pixpa, we decided to rewrite all our themes. 
The current codebase was written in PHP without any framework or MVC approach in mind, basically quite messy. 
To be able to rewrite the themes, we first needed a framework that allowed for easier and faster development. While deciding on the stack to be used, we had these considerations in mind : 

- Moving to a better templating engine for faster development and reusability. Of the may given options, we settled on handlebars. 
    - It has a easier syntax, so that new developers can get up to speed real quick. 
    - It has support in multiple languages, so migrating in the future would be much easier. 
    - It had a very good pre-rendering flow using grunt, hence saving on a bit of runtime. 
- Keeping the build process in the hands of the frontend team, so as they can ensure that the entire assets are as they plan to be. We went along with Grunt without much thinking. 
- Writing the CSS using pre-processor for keeping it modular and reusable. There wasn't much rationale behind using LESS over SASS but our prior experience, we just went ahead with LESS. 

With the basics as to how the Frontend would be managed, we now had to decide on a rendering framework. This would be responsible for using the users' data and rendering the proper HTML for the user. 
This was a rather tricky part, as our platform is basically a DIY website builder, hence the permutations and combinations of the layouts and users' settings are numerous, and whatever rendering pipeline we went ahead with, had to be based on the fact that it can handle all these options and also any new layouts or settings we introduce in the future. 

Our initial debates were over the fact, wether the rendering should be done on the backend or the frontend, though that debate was shortlived as our backend would need quite some time to update itself to incorporate the discussed changes and we had to move fast. 

Moving the rendering to the clientside, again started off a new debate as to which framework should be used. AngularJS, backbone, knockout etc were our choices. 
After reading a lot as to how these frameworks are structured and what to be used in what use case, we decided to go for an in house framework to suit our needs.

- Most of the frameworks are opinionated in how to structure your project. While that's good for people who can comprehend how their project would pan out to be. 

*Write an explanation of why chose a custom framework* 


