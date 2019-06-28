# Keepalived 

空的模版项目

- cp -r Keepalived _**NewProject**_
- cd _**NewProject**_
- rm Keepalived.iml
- sed -i '' 's/Keepalived/_**NewProject**_/g' `grep Keepalived --include=\*.{md,html,xml} -rl .`
- git remote set-url origin https://github.com/hello-world-example/_**NewProject**_.git

