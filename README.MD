# Theorecical Computer Science course at Innopolis University:
This is a repo of [TCS course at the Innopolis University website](https://tcs-iu.netlify.app/). Feel free to contribute!

Table of contents
- [Theorecical Computer Science couse at Innopolis University:](#theorecical-computer-science-couse-at-innopolis-university)
  - [How to contribute](#how-to-contribute)
  - [Familiarize yourself with our techstack](#familiarize-yourself-with-our-techstack)


## How to contribute
If you ***do not have*** the repo on your machine:

- Make sure you have [git](https://git-scm.com/downloads), [hugo](https://gohugo.io/installation/), and any code editor installed ([VSCode](https://code.visualstudio.com/) is recommended, but you may use the one you prefer)
- Clone the repository **with submodules**: 
  ```
  $ git clone --recursive https://github.com/TCS-IU/TCS_labs.git
  ```
  *(Note) If you have already clone this repo without submodules, run this from the source directory*
  ```
  $ git submodule init && git submodule update
  ```
Now you can start contributing:
- To start the website localy, run
  ```
  $ hugo server --minify --theme=hugo-book
  ``` 
- The last line in the terminal output should look like
  ```
  Web Server is available at //localhost:some-port-number/ (bind address 127.0.0.1)
  ```
  Visit `localhost:some-port-number` in your browser to access your local instance of the website. Now all of you changes in the website's source code should be propageted automatically.
- You are ready to rock!!! Make changes and contribute!
- After you feel you have made enough changes, run <br> 
  [`git add .`](https://git-scm.com/docs/git-add),<br>
   then <br>
  [`git commit -m "Your very informative message that describes the changes you've made"`](https://git-scm.com/docs/git-commit). 

  Note that this saves and documents changes on your machine only.
- To propagate your changes to others, run
  ```
  git push origin master
  ```
  *(Note for the experienced contributors) You can run `git push origin master -u` to make `origin master` your default branch to push and pull to.*

**Important note!**

Make sure to run [`git pull`](https://git-scm.com/docs/git-pull) before you make any new changes after you've pushed, so that you avoid creating merge conflicts.
  
## Familiarize yourself with our techstack
- [The world’s fastest framework for building websites | Hugo (gohugo.io)](https://gohugo.io/) - static website generator
- [Introduction | Hugo Book (hugo-book-demo.netlify.app)](https://hugo-book-demo.netlify.app/) - Hugo book theme
- [KaTeX – The fastest math typesetting library for the web](https://katex.org/) - LaTeX compiler
- [PyScript | Run Python in your HTML](https://pyscript.net/) - Client-side python runner embedded in the browser
- [Pynecone: The easiest way to build web apps.](https://pynecone.io/) - Helps us create interactive features with python (WIP)
- [Develop and deploy websites and apps in record time | Netlify](https://www.netlify.com/) - Server host
