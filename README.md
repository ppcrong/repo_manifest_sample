# repo_manifest_sample
sample for git-repo manifest

## git-repo installation

- following installation steps should be ok on **UBUNTU** and **WSL**.
- for installtion on **Windows**, it should be similar but not yet tested, I will try it later and update soon...

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

## about git-repo manifest
- [repo Manifest Format](https://gerrit.googlesource.com/git-repo/+/HEAD/docs/manifest-format.md)

## revision usage in manifest
- list remote references
    ```
    git ls-remote
    8211fb0ac017b20057465ef4a011de2b2707f236	HEAD
    8211fb0ac017b20057465ef4a011de2b2707f236	refs/heads/dev
    5c866785fc35c9f65c437a971f20a5953480d1b6	refs/tags/v1.0
    6e0fd1f7a9b5581e67cd1653b39524b2cae0499f	refs/tags/v2.0
    ```
- set tag
    ```
    <project name="cpp_main" remote="origin" path="apps/cpp_main" revision="refs/tags/    v2.0"/>
    ```
- set commit id
    ```
    <project name="cpp_main" remote="origin" path="apps/cpp_main"     revision="e5f149a90dc6147ab493bc037739dfe15b221259"/>
    ```
