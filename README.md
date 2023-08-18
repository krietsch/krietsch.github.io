# **Personal website of Johannes Krietsch**

### **Description**

This repository contains all data and code associated to [krietsch.github.io](https://krietsch.github.io/). 
The website is made with [R blogdown](https://bookdown.org/yihui/blogdown/), which combines 
[R Markdown](https://rmarkdown.rstudio.com/) and [Hugo](https://gohugo.io/). It is build in the docs/ folder 
and hosted with [Github Pages](https://pages.github.com/). 

### **Short Workflow**


#### New GitHub repository
Create new empty repository named krietsch.github.io (see https://pages.github.com/)

<br>

#### Clone repo to RStudio (assuming Github connection is setup)
File -> New Project -> Version Control -> Git -> enter URL: https://github.com/krietsch/krietsch.github.io

<br>

####  Start website using blogdown (see https://bookdown.org/yihui/blogdown/a-quick-example.html)
install.packages("blogdown")
blogdown::new_site(theme = "wowchemy/starter-hugo-academic") # for academic theme

<br>

####  Look at site locally
blogdown::serve_site()

<br>

####  add .nojekyll file 
file.create(".nojekyll")

<br>

####  change baseURL
baseURL: 'https://krietsch.github.io/'

<br>

####  add publishDir: docs statement below baseurl in the config.yaml
publishDir: docs

<br>

#### build site in doc folder
blogdown::build_site()

<br>

#### commit changes and push to GitHub (only works via terminal, to many big files for RStudio to commit in add-on)
git add .
git commit -a -m "commit message"
git push 

<br>

#### specify for GitHub to build website from docs folder
go to GitHub project (https://github.com/krietsch/krietsch.github.io)
Settings -> Pages -> Build and deployment -> Branch set to /docs

<br>

#### website should be hosted now! Customize as wanted!
check with blogdown::serve_site() local changes
if happy, build site blogdown::build_site()
commit and push to GitHub
