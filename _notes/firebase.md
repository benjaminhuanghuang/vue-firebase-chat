## Create project
Register App

Copy the firebaseConfig into project



## Database
Cloud Firestore -> Create database

Reade data
```
  db.collection('users')
    .doc('PSNArFzFw7wuaMGOu6e3')
    .get()
    .then(snapshot => {
      this.user = snapshot.data().name
    })
```



## Auth
Authentication -> Sign-in method -> enable "Email/Password"


Authentication -> users -> Add user

```
```

