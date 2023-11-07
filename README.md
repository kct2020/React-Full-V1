# React-Full-V1

From <https://github.com/vikejs/vike/tree/main/examples/react-full-v1>

My approach is to use this as a development log. Then rewrite if the project becomes useful.

## 231107 main

This README log.
Next, following amended instructions from the [Vue Full V1 example](https://github.com/vikejs/vike/blob/main/examples/vue-full-v1/readme.md), I will:

```bash
git clone git@github.com:vikejs/vike
cd vike/examples/react-full-v1/
npm install
npm run dev
```

But that fails with:
>Cloning into 'vike'...
The authenticity of host 'github.com (140.82.121.4)' can't be established.
ECDSA key fingerprint is SHA256:p2QAMXNIC1TJYWeIOttrVc98/R1BUFWu3/LiyKgUfQM.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com,140.82.121.4' (ECDSA) to the list of known hosts.
<git@github.com>: Permission denied (publickey).
fatal: Could not read from remote repository.
>
>Please make sure you have the correct access rights
and the repository exists.

So, I'll try the [SVN method for subfolder extraction](https://shantoroy.com/github/download-subfolder-from-github-repository/):

```bash
svn checkout https://github.com/vikejs/vike/trunk/examples/react-full-v1
```

Giving
>bash: svn: command not found

So, I'll try `bash -l` from [stackoverflow]()

gh api \
  -H "Accept: application/vnd.github+json" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  /kct2020/codespaces/secrets/SECRET_NAME/repositories
