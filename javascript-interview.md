## JAVASCRIPT INTERVIEW QUESTIONS AND ANSWERS
### 1. Mapping Users to Get Usernames

```bash
const users = [
  {
    id: 1,
    name: "krishna",
    isActive: true,
    age: 22,
  },
  {
    id: 2,
    name: "somesh",
    isActive: true,
    age: 20,
  },
  {
    id: 3,
    name: "sai",
    isActive: false,
    age: 30,
  },
];
```
#### Q 1.1 Write code to get array of names from given array of users
###### Method 1:
```bash
  const names = [];
  for(let i=0; i<users.length; i++){
    names.push(users[i].name);
  }
  console.log("names", names);
```
###### Method 2:
```bash
  const names = [];
  users.forEach((user) => {
    names.push(user.name);
  });
  console.log("names", names);
```
###### Method 3 ✔:
```bash
  const names = users.map((user) => user.name);
  console.log("names", names);
```
#### Q 1.2 Get back only active users
##### Method 1:
```bash
  const names = [];
  for(let i=0; i<users.length; i++){
    if(users[i].isActive){
      names.push(users[i].name);
    }
  }
  console.log("names", names);
```
###### Method 2 ✔:
```bash
  const names = users.filter((user) => user.isActive).map((user) => user.name);
  console.log("names", names);
```
#### Q 1.3 Sort users by ascending
