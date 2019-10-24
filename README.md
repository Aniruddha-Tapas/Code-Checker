# GitCheck

GitCheck is a web service that can automatically grade your GitHub projects according to standard style guidelines and provide detailed feedback on the breakdown of your major styling mistakes. On top of that, our service gives an overall rating of your profile and each of your repositories. You can see where you specifically need to improve to bring your ratings up and become a better developer. Company recruiters can also easily discover top-tier talent and experience in candidates by searching their ratings with our service.

![GitCheck Screenshot](https://raw.githubusercontent.com/Aniruddha-Tapas/GitCheck/master/gitcheck.jpg)

Input your github profile link to get a code style score and suggestions to improve your coding style.
You can check the webapp out at http://checkgitout.com! 


## Setup
```
npm install
pip install -r requirements.txt
```
Add database password to environment variables
On mac:
Run this in terminal OR add this to ```~/.bashrc```
```
export PENNAPPS_MONGO_PASSWORD="password_here"
```

On windows:
```
setx PENNAPPS_MONGO_PASSWORD password_here
```

## Running
```
node app.js
```
Open browser to ```http://localhost:7000```


### Docker instructions (optional)
Build:
```
docker build -t codechecker . --build-arg mongo_password=<password_here>
```
Run
```
docker run -t -p 7000:7000 codechecker
```
Stop
```
docker stop $(docker ps -a -q --filter ancestor=codechecker --format="{{.ID}}")
```

