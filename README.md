# Lab 2 instructions to upload code to Github

The easiest way to upload code to GitHub is to use the ssh key. The following command can generate a new SSH key:

```
ssh-keygen
```

The generated public key is stored at: `/.ssh/id rsa.pub`

You can view your public key with the following command:
```
cat /.ssh/id rsa.pub
```

Add this public key to your GitHub account using the following steps: `GitHub → Settings → SSH and GPG Keys → New SSH Key → Add your generated public Key → Save.`

You can further secure your SSH key by using a hardware security key, which requires the physical hardware security key to be attached to your computer when the key pair is used to authenticate with SSH. Although it is not necessary and recommended for the class, extra security always helps.

Next configure your username and email with Git using the below commands: 
```
git config −−global user.name GITHUBUSERNAME
git config −−global user.email GITHUB EMAIL
```

Clone the GitHub lab2 repository using the following command: 
```
git clone git@github.com:Foundations-of-Robotics-RBE-500-WPI/lab2.git
```

Then, change directory to your generated folder `lab2`
```
cd lab2
```

Check your current branch by typing:
```
git branch
```

You should see the name of the current pulled branch `main`.

After, create a new branch with your WPI username which is similar to your USERNAME including the `feature/` at the beggining (example, feature/alioulemes)

Thus, type:
```
git checkout -b feature/USERNAME
```

Now add a new python program that prints `Hello World!`

Add this file to the `lab2` repository folder and sync it with GitHub using the following command:
```
git add .
git commit −m `First Commit`
git push
