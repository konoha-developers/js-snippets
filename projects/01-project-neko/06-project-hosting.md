# 6. Project Hosting

### `Step 1️⃣` : Push the code to your github fork once your project is done.

Use the following commands(recommended) to push code on your fork or you can upload your files using the GUI too.

##### 1.0 Initialize git repository if you haven't already

Note - *If you used the `git clone` command while cloning the forked repo then you can skip step no. 1.1 and 1.4*

```sh
git init
```

##### 1.1 Add your changes

```sh
git add .
```
##### 1.2 Check your staged changes

```sh
git status
```

##### 1.3  Commit your Changes

```sh
git commit -m <write commit message inside quotes>
```

##### 1.4 Set the remote(the place where you want to push your code)

First of all copy the remote url from your forked repository

![image](https://user-images.githubusercontent.com/74975876/145529962-d4fc6602-6698-408a-91db-d6228ee3096f.png)

Then use the following commands

```
git remote add origin  <remote_url>
# Sets the new remote
```

```
$ git remote -v
# Verifies the new remote URL
```

##### 1.5 Push to the Branch 

```sh
git push -u origin <branch-name>
```

### `Step 2️⃣` : Follow the below tutorial from step 4 to host your website on github pages.

Note 📃 - **Select your default branch for hosting in step 4.3 in the below tutorial**

[Tutorial](https://github.com/bhavesh-chaudhari/learn-hosting-with-gh-pages#step---4--host-website-from-the-repository)
