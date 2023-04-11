https://www.loginradius.com/blog/engineering/google-authentication-with-golang-and-goth/

### Prereqs

We can create a client ID and client secret using its [Google API Console](https://console.cloud.google.com/apis/dashboard). You need to follow below steps once you open Google API Console

* From the project drop-down, select an existing project, or create a new one by selecting Create a new project
* In the sidebar under "APIs & Services", select Credentials
* In the Credentials tab, select the Create credentials drop-down list, and choose OAuth client ID.
* Under Application type, select Web application.
* In Authorized redirect URI use http://localhost:3000/auth/google/callback
* Press the Create button and copy the generated client ID and client secret

**Note:** If Google doesn't support http://localhost:3000, then use http://127.0.0.1:3000

### Initialize

```
go mod init googleauth

```

### Run

```
export SECRET_SESSION_KEY=""
export GOOGLE_KEY=""
export GOOGLE_SECRET=""
go run main.go
```
