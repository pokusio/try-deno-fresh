## Let's be fresh


### Install `deno`

* Windows (git bash) : 

```bash


choco install deno

export PATH="$PATH:/C/ProgramData/chocolatey/lib/deno"

if [ -f ./.profile.deno.add.on ]; then 
  rm ./.profile.deno.add.on 
fi;

echo '# --- --- ---' | tee -a ./.profile.deno.add.on 
echo '# - Deno' | tee -a ./.profile.deno.add.on 
echo 'export PATH="$PATH:/C/ProgramData/chocolatey/lib/deno"' | tee -a ./.profile.deno.add.on 
deno --version

cat ./.profile.deno.add.on | tee -a ~/.profile | tee -a ~/.shrc | tee -a ~/.bashrc

source ~/.bashrc
```


### Run this Deno/Fresh app

* git clone this repo, and run : 

```bash
deno task start
```

### Start Fresh Quickstart

> see : 
> * https://fresh.deno.dev/
> * https://fresh.deno.dev/


* create project : 

```bash

deno run -A -r https://fresh.deno.dev my-project
# cd my-project
rm ./my-project/README.md
cp -fR ./my-project/* .
rm -fr ./my-project/
deno task start
```

## The Deno SAAS

After I finished the qquickstart, I created an aacount on https://dash.deno.com/ , using github login, and there is there an interesting fast option to try.