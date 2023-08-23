run dev server with 

```bash
cd ./income-tax-refund-blog
hugo server --themesDir ../..
```


build /public/ folder with

```bash
cd ./income-tax-refund-blog
hugo --minify --destination ./public --themesDir ../..
```

publish to gh-pages via

```bash
git worktree add public gh-pages # delete ./public folder if you get an error message and build again before commiting 
hugo --minify --destination ./public --themesDir ../..
cd public
git add .
git commit -m"..."
git push origin gh-pages
```

##### hints on the setup

https://www.andrewhoog.com/post/git-submodule-for-hugo-themes/

https://www.adamormsby.com/posts/000/how-to-set-up-a-hugo-site-on-github-pages-with-submodules/

https://qualityandinnovation.com/2020/12/22/building-your-hugo-site-locally-part-2/

[Publishing a `dist` folder from `master` branch using **worktree** feature to `gh-pages` branch.](https://gist.github.com/lajlev/4b1d0207f87d0a8e9cf20fc78a6fd60a)