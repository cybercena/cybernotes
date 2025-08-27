We can configure Git both locally and globally. If we want to set ownership for a single repository, we configure it locally. If we want the ownership settings to apply to all repositories on the system, we configure it globally.

## Step wise Step Git Configuration

### Step 1: Check if Git is installed
Open your terminal (linux/macOS) or GitBash (Windows):

```bash
git --version
```

if installed, you will see something like :

![](https://raw.githubusercontent.com/cybercena/Static-assets/refs/heads/main/Git_and_Github/gitconfig1.png)

### Step 2 : Configure Git Globally
This sets your identity for all repositories on your system.
```bash
git config --global user.name "username"
git config --global user.email "email@example.com"
```

{% hint style="warning" %}
**Warning:** If you'll push to GitHub and want to keep your email private, use Github's noreply email (e.g., username@users.noreply.github.com)
{% endhint %}
