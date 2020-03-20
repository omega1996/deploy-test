# deploy-test
Say you have a github project and you want to host it on netlify. I’ am just kidding. You are here because you want to host it using github pages.Please follow carefully the following steps:

1. Create a new local branch in your project and name it ‘gh-pages’.
2.  Go to github and copy the name of the repository. Let’s assume the repository name is ‘my-first-project’
3.  Create a new file in root directory of your project and name it ‘vue.config.js’. Why this name? Check out here why.
In ‘vue.config.js’ file paste the following code:
`  
// vue.config.js  
module.exports = {  
publicPath: ‘/my-first-project/’  
}`  
4.  Find and open the file .gitignore located in root directory of your project.Next, find and comment the line which has the text ‘/dist’.
NOTE: this folder it’s ignored by default that’s why we have to comment it.
5.Run npm run build, and wait for it to finish.
IMPORTANT!! Before you run the next command make sure you don’t commit the .gitignore and vue.config.js.
6.Run the command: git add dist && git commit -m "Initial dist subtree commit"
7.Run the command: git subtree push --prefix dist origin gh-pages
8.Navigate to github on your browser and open your repository. Next click ‘Settings’ just like it is displayed below.
9. Scroll and find the section GitHub Pages. Select the ‘gh-pages’ branch and click Save.
10. You might have to wait a while, but if everything goes well you will see the following alert message. Generally you have to wait 8–10 minutes until this process is done
