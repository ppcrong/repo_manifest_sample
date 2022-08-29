# repo_manifest_sample
sample for git-repo manifest

## git-repo installation

**(Ignore if git-repo is installed)**

```sh
# create directory
mkdir -p ~/.bin

# download repo
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo

# add rx mode
chmod a+rx ~/.bin/repo

# open ~/.bashrc
nano ~/.bashrc

# add export path to the end of bashrc
PATH="${HOME}/.bin:${PATH}"

# take effect modified .bashrc
source ~/.bashrc

# check repo version
repo version

# it's ok to show <repo not installed> by 'repo version'
```

## sample.xml
```sh
repo init -u git@github.com:ppcrong/repo_manifest_sample.git -m salmple.xml -b dev --worktree
```

>    * ppcrong/cpp_main
>    * ppcrong/cpp_lib1
>    * ppcrong/cpp_lib2
>    * ppcrong/cpp_lib3
>    * ppcrong/cpp_lib4

