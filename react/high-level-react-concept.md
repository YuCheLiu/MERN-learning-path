# High-level React concept

Declarative vs imperative

Declarative: The goal is to get the result. Not worry about the process.

```javascript
const longPasswords = passwords.filter(password => password.length >= 9);
```

Imperative: line by line to execute the programming.

```javascript
let longPasswords = [];
for (let i = 0; i < passwords.length; i++) {
   const password = passwords[i];
   if (password.length >= 9) {
      longPasswords.push(password);
   }
}
```

Virtual DOM vs traditional DOM



Component-Based design&#x20;

* Components talk to each other by sharing state information.

**Isomorphic**

* **Code can run either on client side and server side.**

****

Babel compiler helps us to transfer JSX file to javascript file



Separation of concerns -> reduce coupling, increase cohesion. Coupling -> the degree to which each program module relies on each of other modules. Template encourage a poor separation of concerns. Template separate technologies not concern
