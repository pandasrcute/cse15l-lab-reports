
# Lab Report 3 
### Written by: Tracy Zhao (A16764072)

---

## Streamlining ssh Configuration
-> Every time we log into our ieng6 account, we have to type `ssh cs15lsp22zzz@ieng6.ucsd.edu`, and that is hard to remember. It is also very long to type especially if we have to log out and back in multiple times in one sitting. That's why ssh has configuration files that can save us from typing this long command.

`.ssh/config` file <br>
This file tells SSH what username to use when logging into specific servers, and even give servers nicknames. I edited it using VScode. <br>
![img1](lr6-1.png)

Now that we have set this up, all we have to do is type `ssh ieng6` to log in. 
![img2](lr6-2.png)

Here is an `scp ` command copying a file into my account
![img3](lr6-3.png)

---

## Setup Github Access from ieng6
-> If you try to use `commit` and `push` this from the command line, you’ll likely see an error. You must use a token-based login mechanism like SSH keys. To fix this, you need to add the public key you made to Github. <br>

These are my public keys that I made from the remote access lab (local) and on ieng6 (remote). (on Github)
![img4](lr6-5new.png) 

Here are the public key and private key (in my local user account).
![img5](lr6-5.png)

Here are the public key and private key (in my remote ieng6 account).
![img5a](lr6-6new.png)

Now using `git` commands to commit and push a change to Github while logged into my ieng6 account.
![img6](lr6-6.png)

Here is the [link](https://github.com/pandasrcute/markdown-parser/commit/7551b75dd2169169129584d8c3185a4d928e3767) for the resulting commit:
![img7](lr6-7.png)

Another example:
![img6a](lr6-7new.png)

Here is the [link](https://github.com/pandasrcute/markdown-parser/commit/dbc839430289b6e5ad118a6fab5c8f2fe497837f) for the second commit:
![img 7a](lr6-7a.png)

---

## Copy whole directories with `scp -r`
-> The command `scp -r` allows us to copy entire directories by recursively copying the directory and all the files and directories within it, and all the files and directories with those, and so on.

Copying my whole markdown-parse directory to my ieng6 account (very long)
![img8a](lr6-8a.png)
![img8b](lr6-8b.png)
![img8c](lr6-8c.png)
![img8d](lr6-8d.png)


Copying all the .java and .md files as well as lib from my markdown-parser directory to my ieng6 account. (shortened)
![img8](lr6-8.png)

Logging into my ieng6 account and compiling and running tests for my repository.
![img9](lr6-9.png)

Combining `scp`, `;`, and `ssh` to copy the whole directory and run the tests in one line.
![img10](lr6-10.png)
