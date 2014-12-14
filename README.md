# Name

Jake White

# How many points have you earned?

~30/100

(Make your own calculation and replace the number 0 with the points you think you've earned.)

# How many hours have you spent on this?

fill-in-your-answer

# When did you first start working on this week's learning challenges?

fill-in-your-answer

# What is the most difficult part about this week's challenge?

getting mongodb to work

# Show and tell (8 points)

## Link (2 points)

[title-of-the-article](http://link-to-an-article-about-machine-learning-use-for-big-data)

## Discuss how you may apply the machine learning technique mentioned in this article to another interesting problem (6 points).

fill-in-your-answer

# D3 IV

## Checkpoints (3 points x 4 = 12 points)

# 1. (3 points)

![image](http://i.imgur.com/klvWVwz.png)

[checkpoint](checkpoint.html)

# 2. (3 points)

![image](http://i.imgur.com/3QfO97Z.png)

[checkpoint](checkpoint.html)

# 3. (3 points)

![image](http://i.imgur.com/6P5r2Mt.png)

[checkpoint](checkpoint.html)

# 4. (3 points)

![image](http://i.imgur.com/jP7jugP.png)

[checkpoint](checkpoint.html)

## Challenges (4 points x 3 = 12 points)

# 1. (4 points)

![image](http://i.imgur.com/zxM02Iq.png)

# 2. (4 points)

![image](http://i.imgur.com/cMh80q2.png)

# 3. (4 points)

![image](http://i.imgur.com/K4V0HpQ.png)

[challenge3](challenge3.html)



# MongoDB II

## Checkpoints (6 points x 2 = 12 points)

### 1 (6 points)

[mongodb js code collecting github events about our course](mongodb_github.js)

### 2 (6 points)

![terminal output of mongodb query](http://i.imgur.com/Zsam0vj.png)

## Challenge 1 (4 points x 10 = 40 points)

### 1 (4 points)

> db.gitEvents.findOne({"actor.login":"doubleshow"})

![screenshot](http://i.imgur.com/kYELz6S.png)

### 2 (4 points)

> db.gitEvents.findOne({"actor.login":"doubleshow"},{'actor':1})

![screenshot](http://i.imgur.com/GEtNE6G.png)

### 3 (4 points)

> db.gitEvents.find({'actor.login':{$in:['doubleshow','chrisbopp']}}, {'actor.login':1,'created_at':1})

![screenshot](http://i.imgur.com/DaxoKoA.png)

### 4 (4 points)

> db.gitEvents.findOne({‘type’:’PushEvent’})

![screenshot](http://i.imgur.com/aj7UXQv.png)

### 5 (4 points)

db.gitEvents.distinct('payload.commits.author.name', {'type': 'PushEvent'})

![screenshot](http://i.imgur.com/yNYOgaY.png)

### 6 (4 points)

b.gitEvents.findOne({'type': 'IssueCommentEvent'},{'payload':1})

![screenshot](http://i.imgur.com/uYdRxbM.png)

### 7 (4 points)

db.gitEvents.distinct('payload.issue.user.login', {'type': 'IssuesEvent'})

![screenshot](http://i.imgur.com/3DCDQaf.png)

### 8 (4 points)

> db.gitEvents.find({'type':'IssuesEvent', 'payload.issue.state':'closed'}, {'payload.issue.id':1, 'payload.issue.state':1})

![screenshot](http://i.imgur.com/bOBo8V9.png)

### 9 (4 points)

> db.gitEvents.find({'type':'IssuesEvent', 'payload.issue.state':'open'}, {'payload.issue.user.login':1, 'payload.issue.state':1})

![screenshot](http://i.imgur.com/my0IxQC.png)

### 10 (4 points)

> db.gitEvents.find({'type':'IssuesEvent', 'payload.issue.comments':{$gt:0}}, {'payload.issue.user.login':1, 'payload.issue.comments':1})

![screenshot](http://i.imgur.com/2Q5cZkR.png)


## Challenge 2 (8 points x 2 = 16 points) 

### 1 (8 points)

Number of issues mike has commented on: 8

> db.gitEvents.find({'type': 'IssuesEvent', 'payload.issue.user.login':'wannabeCitizen'}).count()

![screenshot](http://i.imgur.com/XIEzlLz.png)

### 2 (8 points)

Total number of issue comments

> db.gitEvents.find({'type': 'IssueCommentEvent'}).count()

![screenshot](http://i.imgur.com/yfXpuuC.png)
