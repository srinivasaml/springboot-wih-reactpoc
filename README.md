# Your First Full Stack Application with React and Spring Boot

## Take your first steps towards becoming a Full Stack Developer with React and Spring Boot

React is a one of the most popular front end view frameworks

In combination with other libraries, React helps in doing a wide variety of front end features

- Forms Handling
- Routing System
- HTTP Requests

Spring Boot is an awesome framework to build RESTful API and Microservices.

## Installation Guides

#### Required Tools

- Node v8+ for npm
- Visual Studio Code - Latest Version
- Java 8+
- Eclipse - Oxygen+ - (Embedded Maven From Eclipse)

### Getting Started with Spring, Spring Boot and JPA

- Spring Tutorial for Beginners - https://www.youtube.com/watch?v=edgZo2g-LTM
- Spring Boot Tutorial for Beginners - https://www.youtube.com/watch?v=pcdpk3Yd1EA
- JPA and Hibernate Tutorial for Beginners - https://www.youtube.com/watch?v=MaI0_XdpdP8

- Running Examples

  - Download the zip or clone the Git repository.
  - Unzip the zip file (if you downloaded one)
  - Open Command Prompt and Change directory (cd) to folder containing pom.xml
  - Open Eclipse
    - File -> Import -> Existing Maven Project -> Navigate to the folder where you unzipped the zip
    - Select the right project
  - Choose the Spring Boot Application file (search for file with @SpringBootApplication)
  - Right Click on the file and Run as Java Application
  - You are all Set
  - For help : use our installation guide - https://www.youtube.com/playlist?list=PLBBog2r6uMCSmMVTW_QmDLyASBvovyAO3

### Request URLs and Examples

#### Common Headers

```
Origin - http://localhost:4200
Content-Type - application/json
Authorization
- Bearer *** or
- Basic *****
```

#### Retrieve all todos for a user

- GET - http://localhost:8080/users/in28minutes/todos

```
[
  {
    id: 1,
    username: "in28minutes",
    description: "Learn to Dance 2",
    targetDate: "2018-11-09T12:05:18.647+0000",
   : false,
  },
  {
    id: 2,
    username: "in28minutes",
    description: "Learn about Microservices 2",
    targetDate: "2018-11-09T12:05:18.647+0000",
   : false,
  },
  {
    id: 3,
    username: "in28minutes",
    description: "Learn about React",
    targetDate: "2018-11-09T12:05:18.647+0000",
   : false,
  },
]
```

#### Retrieve a specific todo

- GET - http://localhost:8080/users/in28minutes/todos/1

```
{
  id: 1,
  username: "in28minutes",
  description: "Learn to Dance 2",
  targetDate: "2018-11-09T12:05:18.647+0000",
 : false,
}
```

#### Creating a new todo

- POST to http://localhost:8080/users/in28minutes/todos with BODY of Request given below

```
{
  "username": "in28minutes",
  "description": "Learn to Drive a Car",
  "targetDate": "2018-11-09T10:49:23.566+0000",
  "done": false
}
```

#### Updating a new todo

- http://localhost:8080/users/in28minutes/todos/1 with BODY of Request given below

```
{
  "id": 1
  "username": "in28minutes",
  "description": "Learn to Drive a Car",
  "targetDate": "2018-11-09T10:49:23.566+0000",
  "done": false
}
```

#### Delete todo

- DELETE to http://localhost:8080/users/in28minutes/todos/1

### JWT Authenticate

- POST to http://localhost:8080/authenticate

```
{
  "username":"ranga",
  "password":"password@!23@#!"
}
```

Response

```
{
"token": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJyYW5nYSIsImV4cCI6MTU0MjQ3MjA3NCwiaWF0IjoxNTQxODY3Mjc0fQ.kD6UJQyxjSPMzAhoTJRr-Z5UL-FfgsyxbdseWQvk0fLi7eVXAKhBkWfj06SwH43sY_ZWBEeLuxaE09szTboefw"
}
```

Other URLS

- Refresh - http://localhost:8080/authenticate

### Useful Links

- [in28minutes](http://www.in28minutes.com)
- [github](https://github.com/in28minutes/full-stack-with-react-and-spring-boot)

## Connection to MySQL

```
create sequence hibernate_sequence start with 1 increment by 1

create table todo (
    id bigint not null,
    description varchar(255),
    is_done boolean not null,
    target_date timestamp,
    username varchar(255),
    primary key (id))

```

## Next Steps

- React
  - Why we need to bind event handlers in Class Components in React?
    - https://medium.freecodecamp.org/this-is-why-we-need-to-bind-event-handlers-in-class-components-in-react-f7ea1a6f93eb
  - class vs className - A discussion
    - https://stackoverflow.com/questions/46989454/class-vs-classname-in-react-16
  -
- Modern JavaScript
  - https://github.com/mbeaudru/modern-js-cheatsheet#tdz_sample
  - https://learnxinyminutes.com/docs/javascript/
  - https://github.com/mjavascript/mastering-modular-javascript/blob/master/chapters/ch01.asciidoc
  - https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript
  - Modern Javascript Quickly - https://gist.github.com/gaearon/683e676101005de0add59e8bb345340c
- React
  - https://raw.githubusercontent.com/reactjs/reactjs.org/master/static/html/single-file-example.html
  - class vs className - https://stackoverflow.com/questions/46989454/class-vs-classname-in-react-16
  - https://engineering.musefind.com/react-lifecycle-methods-how-and-when-to-use-them-2111a1b692b1
  - https://reactjs.org/blog/2018/03/29/react-v-16-3.html#component-lifecycle-changes
