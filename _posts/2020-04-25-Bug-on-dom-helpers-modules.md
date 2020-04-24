---
layout: blog
title: Bug on dom-helpers module.
category: dev
tags: [ReactJS, MaterialUI, Todo]
summary: How to fix bug on dom-helpers module
image: /images/blog/tip.jpg
---
Today, I tried to build a small project with ReactJS, using Material-UI framework and webpack. But when I try to run the build 
command, it showed this error message:

```
ERROR in ../node_modules/react-transition-group/esm/CSSTransition.js
Module not found: Error: Can't resolve 'dom-helpers/addClass' in '.../node_modules/react-transition-group/esm'
 @ ../node_modules/react-transition-group/esm/CSSTransition.js 5:0-47 13:11-22
```
It's not comfortable with me, because I know there is a conflicting in version of `dom-helpers`. After checked, I realized Material-UI
has react-transition-group dependency of dom-helpers "5.1.3", and there are other modules, which is using lower version of `docker-helpers`. 

So I fix that bug like this:
1. Install fake package dom-helpers@5.1.4 accessible with other name
```
"dom-helpers5": "npm:dom-helpers@5.1.4"
```
2. Add alias in projects's webpack for accessing dom-helpers
```
resolve: { ... alias: { 'dom-helpers': 'dom-helpers5' } },
```

3. Rebuild again. And, booom. It worked like charm.

Hope above solution could help you also.
