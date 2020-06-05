![Hugo logo](/content/images/sample-image.png)

### What

A minimally working example of a static website with [Hugo](https://gohugo.io/) and the [LoveIt](https://themes.gohugo.io/loveit/) theme.

### Why

JS is slow, heavy, and [not secure](https://medium.com/@dhtmlx/security-of-javascript-applications-1c95cd2ce533). When speed is crucial nothing beats plain-old HTML, the only catch is that html is not human friendly. Static website generators solve this problem by letting humans write the content in their markup language of choice, and automatically compiling html code based on configurable rules.

### Hugo

There are [countless](https://www.staticgen.com/) [static generators](https://github.com/myles/awesome-static-generators) out there. Before Hugo I worked with Jekyll and overall [liked it](https://www.resume.lorismarini.dev/) (see the corresponding [template](https://github.com/LorisMarini/jekyll-resume)). However, the build speed of Hugo is hard to resist. Hugo is written in GoLang, a highly-concurrent, statically-typed, lightweight, programming language developed by Google and release at around 2012.

### Try it

1. [install hugo](https://gohugo.io/getting-started/installing)
1. clone and cd into this repository, then run:

`hugo server --buildDrafts --disableFastRender`

and open your browser to http://localhost:1313.

### Build it yourself

The code below uses [GitLab](https://gitlab.com/users/sign_up) but should work just as well with any other cloud git repository.

1. If needed, [install git](https://git-scm.com/downloads) and [install hugo](https://gohugo.io/getting-started/installing)
1. Create a new blank project in GitLab:
1. Open terminal and execute this:

```zsh
# Move to the folder that will contain your new blog
cd ~/projects

# Init the project (this will create a folder called my-website)
hugo new site my-website

# Move inside the folder
cd my-website

# Initialize a git repository
git init

# Tell git about the remote repo in Gitlab (change link with your details)
git remote add origin git@gitlab.com:<gitlab-username>/<project-name>.git

# Add, commit and push
git add . & git commit -m "Initial commit" & git push -u origin master

# Add a theme as a submodule (we use LoveIt out of many https://themes.gohugo.io/)
git submodule add https://github.com/dillonzq/LoveIt themes/LoveIt

# Add a .gitignore file to avoid committing garbage
echo "# Hugo default output directory
/public

# OSX
.DS_Store" > .gitignore

```

If everything went well, you should have a working git repository on your machine as well as on GitLab. To start working open the current directory with your favourite editor and start adding a post (example: example.md) inside content/posts.


## Hard bits

It takes a while to understand Hugo and LoveIt is a fairly advanced theme. If this is your first hugo project I recommend starting with a simpler theme such as [Ananke.](https://themes.gohugo.io/gohugo-theme-ananke/) Remember that each theme requires a different config.toml file. If you don't know where to start look inside the `themes/themeName/exampleSite` to get an idea.

## More Reading
- My post on [Getting started with Hugo and Netlify](https://lorismarini.dev/hugo-and-netlify/)
- My post on [Hugo Tips](https://lorismarini.dev/hugo-tips/)
