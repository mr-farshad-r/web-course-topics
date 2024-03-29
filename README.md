# Web and Application Course Topics

Email me your comments: farshadroozbahani20@gmail.com

[Introduction of  Web, Internet, Programming languages](Introduction/README.md)

[Front-End](Front-End/README.md)
[Package Managers](PackageManagers/README.md)

 - Build tools and Task runner
    - Introduction 
    - Webpack
    - Parcel
 - SPA vs MPA
 - Transpiler
 - Linter
 - Progressive Web Applications (PWA)

## React 

- Introduction 
- Hello World!
- Bad Pattern Development 
- Boilerplate 
- Create and Rendering elements
- JSX
- Java Script Expression 
- Fragment 
- Components
  - Class 
  - Functional

- Props
  - Default props
  - Prop types

- State
- Lifecycles
- Handle events
- Conditional rendering 
- List and Keys
- Forms
- Refs 
  - Create ref
  - Forwarding ref
  - useRef

- Default props
- Code Splitting 
- Controlled and Uncontrolled 
- Higher Order Component (HOC)
- Error Boundaries
- Render props
- Portals
- Routing 
  - React router dom 
    - Browser router 
    - Hash router 
    - Router
    - Route
    - Link
    - Navigate
    - Outlet
    - Hooks method

- XHTTP Requests
  - Fetch 
  - Axios 

- Styling and Visual libraries 
  - Reactstrap
  - Mui 
  - Fluent 
  - Antd
- Hooks
  - useState
  - useEffect 
  - Custom Hooks
  - Rules of hooks
- State managers
  - Redux 
    - Introduction 
    - Reducer
    - Actions
    - Connect
    - Redux hooks 
    - Redux toolkit 
  - Context API
    - Provider 
    - Consumer
- Form Handling 
  - Formik 
  - React Form 

- Validation 
  - Yup 
  - Joi

- React application structure <small> *(npx create-react-app --template structure)* </small>
- Build and deploy React application
- TypeScript
  - Installation
  - Configs 
  - Type
    - Primitive 
    - Object literal 
    - Tuple 
    - Union 
    - Intersection
    - Indexing
    - From value 
    - From functions return 
    - From Module
    - Mapped 
    - Conditional 
    - Template union types

  - Interface 
    - Built-in type
    - Common Built-in type
    - Literal type
    - Avoid
    - Extends
    - Optional 
    - Readonly
    - Generics
    - Getter and Setter

  - Control Flow
    - Typeof 
    - Instanceof 
    - In 
    - Is

  - Class
    - Private 
    - Implements
    - Abstract
    - Decorators and Attributes


## Server Side Rendering (SSR) (_Under Construction_)

- Introduction Next JS
- Pages and Routing 
- Data fetching 
- Assets
- Pre-rendering 
- Deploy

## Mobile Application with React Native  (__Under Construction__)

- Introduction 
- Setup environments
- Components
- Styling
- Build 

## Desktop Application with Electron (_Under Construction_)

- Introduction 

## CLI Application (_Under Construction_) 

- Introduction

## Backend 

- Basic Front-End Knowledge
  - HTML
  - CSS
  - JavaScript
- OS and General Knowledge
  - Terminal usage 
  - Process management 
  - Threads and Concurrency
  - Memory management 
- I/O Management 
- Request and Response
- SSH
- Basic networking concept
- Choose a backend language 
- Learn databases 
  - SQL based
  - NoSQL based
  - Key / Value store
- Web Security Knowledge
- Caching 
- API 
- Architectural patterns
- Message Brokers and Realtime Protocols
- Containerization and Virtualization 
- Web Servers

## Node JS :heart:

- Node Environments
- V8 Engine
- Synchronous vs Asynchronous 
- Event-Driven
- Non Blocking I/O
- Event Queue
- Installation 
- Node and Package managers
- Module System
- File System (FS)
- Operating System (OS)
- Hyper Text Transfer Protocol (HTTP)
- NodeJS Frameworks and libraries 
  - Express JS 
    - Installation 
      - Express Generator
    - Hello World!
    - Static files
    - Middleware 
    - Template Engine 
      - PUG
    - Routing system
    - JSON Web Token (JWT)
    - Connect to database 

## Database (_Under Construction_)

- Introduction
- Database types
  - Relational DBMS (Database Management System)
  - Document Stores
  - Key/Value Stores
  - Graph DBMS
  - Search Engines
  - ...

### MySQL (_Under Construction_)

- Introduction
- Installation 
- Table 
- Column types
- SELECT 
- UPDATE
- DELETE
- INSERT
- Count
- Distinct
- Condition
- Order By
- Like

### MongoDB (_Under Construction_)

- Introduction
- Sharding and Replication 
- Object ID
- Find 
- Find All
- Insert 
- Update 
- Remove

### Redis (_Under Construction_)

- Introduction
- Using basic queries

### Deploy (_Under Construction_)

- Introduction
- PM2
- Nginx Reverse Proxy 
- Docker
- Monitor application 

### Docker (_Under Construction_)

- Introduction

## PHP (_Under Construction_)

- Introduction
  - Frameworks and Libraries 
    - CodeIgniter
    - Laravel

## Python (_Under Construction_)

- Introduction
  - Frameworks and Libraries
    - Flask
    - FastAPI

## Version Control System (VCS) - GIT
- Introduction
- Repository
  - Local
  - Remote
- init ```git init```
- status ```git status```
- add ```git add FILE_NAMEs```
- commit ```git commit -m "MESSAGE"```
- log ```git log```
- diff 
  - diff with HEAD ```git diff HEAD```
  - diff with stage ```git diff --staged```
- reset ```git reset FILE_NAMEs```
- checkout
  - remove file from stage ```git checkout -- FILE_NAME```
  - checkout from tag ```git checkout TAG_NAME```
- branch 
  - list ```git branch```
  - create ```git branch BRANCH_NAME```
  - delete ```git branch -d BRANCH_NAME```
- merge ```git merge BRANCH_NAME```
- rm ```git rm FILE_NAME```
- clone ```git clone GIT_REPOSITORY_ADDRESS```
- push ```git push origin BRANCH_NAME```
- pull ```git pull origin BRANCH_NAME```
- remote 
  - list ```git remote``` ```git remote -v``` 
  - add ```git remote add origin GIT_REPOSITORY_ADDRESS```
- show ```git show [COMMIT_HASH or TAG_NAME]```
- tag 
  - list ```git tag```
  - create ```git tag -a VERSION -m "MESSAGE"```
  - create from commit name ```git tag -a VERSION COMMIT_HASH -m "MESSAGE"```
  - search ```git tag -g "SEARCH_PATTERN"```
  - push tags ```git push origin TAG_NAME``` ```git push origin --tags```
- blame ```git blame FILE_NAME -L LINE_NUMBER```
- bisect
  - ```git bisect start```
  - ```git bisect bad```
  - ```git bisect good COMMIT_HASH```

## Other (_Under Construction_)

- Basic Terminal Usage
  - Navigation 
  - Manipulate files and directory
  - Run CLI applications
- Data Structure and Algorithms
- Semantic Versioning 
- Design Patterns
- Web Security 
- CORS