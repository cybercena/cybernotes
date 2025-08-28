We can configure Git both locally and globally. If we want to set ownership for a single repository, we configure it locally. If we want the ownership settings to apply to all repositories on the system, we configure it globally.

## Check if Git is installed
Open your terminal (linux/macOS) or GitBash (Windows):

```bash
git --version
```

if installed, you will see something like :

![](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Git_and_Github/gitconfig1.png)

## Configure Git Globally
This sets your identity for all repositories on your system.
```bash
git config --global user.name "username"
git config --global user.email "email@example.com"
```

{% hint style="warning" %}
**Warning:** If you'll push to GitHub and want to keep your email private, use Github's noreply email (e.g., username@users.noreply.github.com)
{% endhint %}

![](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Git_and_Github/gitconfig2.png)

![](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Git_and_Github/gitconfig3.png)

## Configure Git Locally
### Step 1 : Create a Repository
Make a directory ``gitproject `` and navigate to folder and initialize the git repo with command ``git init``.

```bash
mkdir gitproject
cd gitproject
git init
```

![creating a gitproject folder](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Git_and_Github/gitconfig5.png)

![Change the working directory to gitproject](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Git_and_Github/gitconfig6.png)

![Initialize the git hub repo](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Git_and_Github/gitconfig7.png)

if you want to push local repo to GitHub, you can learn from [here](https://notes.sonam.info.np/git-and-github/push-to-github)
### Step 2 : Configure the Git locally
- We can use `--local` instead of `--global` in the configuration to configure the git repo locally.

```bash
git config --local user.name "username"
git config --local user.email "email@example.com"
```

![](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Git_and_Github/gitconfig8.png)

## View Git Configuration
-  If you want to view Global Configuration, use command :
```bash
git config --global --list
```

it will show you configuration details :

![](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Git_and_Github/gitconfig4.png)

- If you want to view Local Configuration, navigate the repo folders and run the command :
```bash
git config --local --list
```

![](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Git_and_Github/gitconfig9.png)

