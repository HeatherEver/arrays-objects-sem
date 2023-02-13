start with learning objectives

---

open excalidraw and ask them to name **primitive data types**

- Number
- String
- Boolean
- Null
- Undefined
- Symbol (we're not using much)
- bigInt (we're not using much)

and **non-primative/compound** (name of the session)

- Arrays - type of object but is an ordered list
- Objects
- Functions - come under this object bracket but they are a **compound** data type as they use our **primitive** data types to do other things with

---

---

---

**Switch to VSCode**

have 3 variables already written (crisps)

```javascript
const crisps1 = "quavers";
const crisps2 = "skips";
const crisps3 = "nik naks";
```

`console.log` the crisps - **ASK** what's not so great about declaring them this way
`console.log(crisps1, crisps2, crisps3)`

- spelling errors - human errors
- DRY - very repetitive

---

---

---

declare an array called crisps
`const crisps = ["quavers", "skips", "nik naks"]`

`console.log(crisps) `

we get them now written out as a string with comma's separating them

---

---

---

**PREDICTION TIME**

`crisps[1] = "pringles"`

_do we think we will see 'pringles'??_

pop your answers in the chat - y/n
talk about whats going on in the chat and then have a look at the answer.

`console.log(crisps) -> [ 'quavers', 'pringles', 'nik naks' ]`

we _DO_ get pringles, we have _mutated_ the array. Arrays are _mutable_ which means we can mutate them and we have modified the original array.

We've used `const` which may confuse you but JavaScript only cares about the array itself not changing and not what's inside the array.

---

---

---

**change** `crisps[1]` to be `crisps[10]

---

**ask** what they think y/n

**ask** someone if they feel comfortable enough to explain why we will/won't see 'pringles'

(we don't have an index 10 so it won't run)
however!

---

```javascript
["quavers"
"skips"
"nik naks"
<7 empty items>
"pringles"
]
```

---

we do get pringles but there are 7 empty items.
You've all thought about this correctly that there is nothing to reassign here but we are _mutating_ not **reassigning**

`crisps[100] = pringles`

The length of an array is dictated by it's contents rather than the original length

**sparse array** as it has 97 commas where they are empty items

JavaScript does not care about the contents of an array just that it is an array

---

---

---

**QUESTIONS**

---

---

---

Move onto _METHODS_

**What if we wanted to add an item to the end of our array?**

---

---

---

**open MDN docs**
Go to array methods - go to push

`crisps.push("pringles")`

`console.log(pringles)`

show that `pringles` has been added to the array

`const length = crisps.push('pringles')`

but if we assign this a value and then console log it we also get the _return_ value of the _length_ of our array.

`console.log(length)`

---

---

---

---

**What if i wanted to get rid of party ring from the start of our array???**
possible suggestions...

- _.pop()_ - show it taking something off the end, look in MDN docs too. Assign as variable and you can see the popped item

---

- _.unshift()_ - the first item still stays, unshift _adds_ to the _start_ of an array - use MDN docs again

---

- **.shift()** - yay! shifted something off the start of the array. Look on MDN for a _return value_. We can save to variable to still have access to that value.

---

---

---

**NESTED ARRAYS**

Arrays can also contain other arrays

```
const films = [
    ["Batman Begins", "The Dark Knight", "The Dark Knight Rises"],
    ["Shaun of the Dead", "Hot Fuzz", "The World's End"],
    ["The Little Mermaid", "The Little Mermaid 2: Return to the Sea", "The Little Mermaid: Ariel's Beginning"]
]
```

---

---

---

Lets access the best film on here - _the little mermaid_ of course...
how would we access this as it's nested inside another array?

`console.log(films[2][0])`

ADD `["Ariel", "Flounder", "Sebastian"]` into the mermaid array and ask someone to find **Flounder**
`console.log(films[2][2][1])`

---

---

---

**QUESTIONS**

---

---

---

**OBJECTS**

We now know about arrays - they are ordered collections of data we can use for storing multiple items. There are _limitations_ to the use of ordered collections...

`const details = ["Heather", 28, "Blackpool", true]`

This array is storing all of my important data... but - _what is wrong with this?_
We can only access these by their index position... so what could we use instead?

_an object !!_
An object is a collection of _Key-Value_ pairs called _properties_. Let's make our array into an object

```javascript
const person = {
  name: "Heather",
  age: 28,
  hometown: "Blackpool",
  isCool: true,
};
```

---

---

---

**ACCESSING OBJECTS**

Objects access refers to the process of **"looking up"** or accessing property values using a property key!

_Does anybody know how we could access my name from this object?_

`console.log(person.name)` ---> Heather

---

---

We are using dot notation here to access a property's value by stating the name of the object (person) writing a dot `.` and then adding the _key_ of the value we want to access.

**Let's imagine we want to know what my job is....**
`console.log(person.job)`

_what do we think will be logged in this case??_

\***\*undefined\*\*** because it does not exist!

---

---

However we can add it in - _does anyone know how we could add this property to our object?_

`person.job = "Northcoders"`
`console.log(person)`

---

---

---

---

**DYNAMIC ACCESS**

```javascript
const phonebook = {
  eli: "0789325792",
  alex: "0732598725",
  katherine: "07274652398",
  kirsty: "071387462871",
};

const name = "katherine";
```

---

---

---

_what do we think will happen when we run..._
`console.log(phonebook.name)` .... // undefined

_WHY_ - we've used the actual string version of `name` rather than the variable

_does anyone know how we could use this variable to access the property we want?_

`console.log(phonebook[name])` .... // "07274652398"

---

---

---

---

EXPLAIN WEDNESDAYS
NO NCHELP
KATAS
WE PROVIDE
