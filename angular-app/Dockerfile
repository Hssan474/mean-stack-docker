Skip to content
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@Hssan474 
radhouen
/
mean-stack-docker
3
613
Code
Issues
3
Pull requests
1
Actions
Projects
Wiki
Security
Insights
You’re making changes in a project you don’t have write access to. Submitting a change will write it to a new branch in your fork Hssan474/mean-stack-docker, so you can send a pull request.
mean-stack-docker
/
angular-app
/
Dockerfile
 

Spaces

2

No wrap
1
# Stage 1
2
FROM node:8.11.2-alpine as node
3
​
4
WORKDIR /usr/src/app
5
​
6
COPY package*.json ./
7
​
8
RUN npm i npm@latest -g
9
​
10
RUN npm install
11
​
12
COPY . .
13
​
14
RUN npm run build
15
​
16
# Stage 2
17
FROM nginx:1.13.12-alpine
18
​
19
COPY --from=node /usr/src/app/dist /usr/share/nginx/html
20
​
21
COPY ./nginx.conf /etc/nginx/conf.d/default.conf
22
​
@Hssan474
Propose changes
Commit summary
Create Dockerfile
Optional extended description
Add an optional extended description…
 
© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
