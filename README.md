# overthewire
This is to show level by level right up of OverTheWire Bandit War Geams.

## Bandit 0
The goal is to use SSH to contact bandit.labs.overthewire.org on port 2220. 

I started with understanding SSH with the link provided on overthewire which took me to the SSH manual page. 

![image](https://github.com/reickcs/overthewire/assets/119334123/eb149a5a-14cb-4c7c-a0ea-5013482a3d3e)


In the man page I found "-p" to specify the port. Looking at how the syntax should be like this:

ssh bandit0@bandit.labs.overthewire.org -p 2220

I was then prompted for a password for which I put bandit0. 

![image](https://github.com/reickcs/overthewire/assets/119334123/444aca42-7187-4007-8d81-9f77207952de)

I successfully gained access to the first level. 

![image](https://github.com/reickcs/overthewire/assets/119334123/a630a3ef-e9ab-46e9-9b89-d507554916d4)


## Bandit 1

The password for the next level is in a file for readme located within the home directory. I need to find the file, read the file, and get the password to then SSH into the next level. 

I was given several options that I could use to solve this level.
  ls
  cd
  cat
  file
  du
  find

Based upon going through manual pages, I found that ls, and cat are the two commands that will help me solve this problem. 

first I listed the file contents of my current directory. Found the readme file and then used cat to read the contents.

![image](https://github.com/reickcs/overthewire/assets/119334123/0e71a1f2-d2e6-40e6-8c0d-02b2050aaaa5)


I proceeded to copy the password for future reference

- <details><summary>The password is:</summary>
  <pre>
  NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
  </pre>
  </details>
