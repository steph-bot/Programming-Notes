# Programming Notes

Hi, I'm Stephanie! I work as a software support engineer at a startup in Houston, TX. I started my career as a chemical engineer in process automation design for a major chemical corporation. After a car accident left me seriously injured, I fell in love (again) with web development. I worked through online classes and projects in between doctor's appointments and physical therapy and am now working on becoming the best engineer I can be :-)

I created most these notes to supplement video lectures and tutorials by Andrei Neagoie. It's nice to have a personal reference written in my own words with my own code samples. 

- Notes from Code Complete 2 by Steve McConnell
- A great notes reference: https://github.com/mgp/book-notes/blob/master/code-complete.markdown
- My favorite CSS commenting styles: https://cssguidelin.es/
- Google JS Style Guide: https://google.github.io/styleguide/jsguide.html
- Ant Design (React UI Library) https://ant.design/
- Mocha vs Jest
- Chai, Should
- Code coverage tools: nyc (Istanbul)
- TypeScript: https://www.typescriptlang.org/docs/handbook/basic-types.html
- ESLint (AirBnB)
- Readme template: https://www.makeareadme.com/
- Funny article about Babel: https://hackersandslackers.com/babel-ecma-script/
- ASCII One Liners: https://www.asciiart.eu/ascii-one-line
- https://remotepoc.com/
- General Clean Code guidelines as they apply to typescript: https://github.com/labs42io/clean-code-typescript
- npm linking:
```
cd inspector-dev-tools # <-- whichever directory has the package
npm link
cd sophos-central-inspector
npm link @liongard/inspector-dev-tools # <-- this installs from your local drive and not from npm basically
```
- Some very cool AWS labs: https://github.com/acantril/learn-cantrill-io-labs
- Manually kill Node process in terminal:
```
pkill -9 node
```
- macOS – SSH Error ‘No Matching Exchange Method Found’: https://www.petenetlive.com/kb/article/0001245

<br>
<br>
<br>
<br>
<br>
To Do:<br>
- Table of Contents
<br>
<br>


## Favorite Comments + ASCII Art
Waves:
```
   _.~"~._.~"~._.~"~._.~"~._
```

Blocky:
```
  ////////////////////
  //   Code Block!  //
  ////////////////////
  ```

Pretty Headingz:
```
  /*----------------------------------------------------------*\
      # PRETTY HEADING HERE
  \*----------------------------------------------------------*/
  ```
  
  ## SOLID + YAGNI
  Single Responsibility Principle
  - A class should have only a single responsibility
  - Only one potential change in the software's specification should be able to affect the specification of the class
  
  Open Closed Principle
  - A module should be open for extension but closed for modification
  
  Liskov Substitution Principle
  - Objects in a program should be replaceable with instances of their subtypes without altering the correctnes of that program
  
  Interface Segregation Principle
  - Clients should not be forced to depend upon the interfaces that they do not use
  
  Dependency Inversion Principle
  - Program to an interface, not to an implementation
  - Use an abstract interface to separate business logic from concrete implementations.
  
  YAGNI
  - You ain't gonna need it: Implement it when you need it, not when you foresee that you may need it.
  - SOLID tells you how to do it, YAGNI tells you when to do it



