# Template 

空的模版项目

- cp -r Template _**NewProject**_
- cd _**NewProject**_
- rm Template.iml
- sed -i '' 's/Template/_**NewProject**_/g' `grep Template --include=\*.{md,html,xml} -rl .`
- git remote set-url origin https://github.com/hello-world-example/_**NewProject**_.git

