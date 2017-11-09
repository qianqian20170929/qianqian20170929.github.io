---
layout: post
title: "hello octopress"
date: 2017-11-09 17:00:09 +0800
comments: true
categories: 
---

## 创建blog

创建blog Octopress的命令，都是通过rake来执行的，接下来，咱们来看一下Octopress提供了哪些功能？执行rake -T，来查看所有的任务命令，可以看到有如下的输出：
```
rake clean                     # Clean out caches: .pygments-cache, .gist-cache, .sass-cache
rake copydot[source,dest]      # copy dot files for deployment
rake deploy                    # Default deploy task
rake gen_deploy                # Generate website and deploy
rake generate                  # Generate jekyll site
rake install[theme]            # Initial setup for Octopress: copies the default theme into the ...
rake integrate                 # Move all stashed posts back into the posts directory, ready for...
rake isolate[filename]         # Move all other posts than the one currently being worked on to ...
rake list                      # list tasks
rake new_page[filename]        # Create a new page in source/(filename)/index.markdown
rake new_post[title]           # Begin a new post in source/_posts
rake preview                   # preview the site in a web browser
rake push                      # deploy public directory to github pages
rake rsync                     # Deploy website via rsync
rake set_root_dir[dir]         # Update configurations to support publishing to root or sub dire...
rake setup_github_pages[repo]  # Set up _deploy folder and deploy branch for Github Pages deploy...
rake update_source[theme]      # Move source to source.old, install source theme updates, replac...
rake update_style[theme]       # Move sass to sass.old, install sass theme updates, replace sass...
rake watch                     # Watch the site and regenerate when it changes
```

## 发布流程
```
rake new_post[’title’]     # 新建博文文件
rake generate              # 将编辑好的博文生成网页
rake preview               # 提交前可以进行本地预览
rake deploy                # 将博文部署到Github上
git commit -a              # 提交本地更改的文件
git push origin source     # 将源文件push到Github的source分支
```
