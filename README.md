# overthewire
This is to show level by level right up of OverTheWire Bandit War Geams.

## Bandit 
The goal is to use SSH to contact bandit.labs.overthewire.org on port 2220. 

I started with understanding SSH with the link provided on overthewire which took me to the SSH manual page. 

![image](https://github.com/reickcs/overthewire/assets/119334123/eb149a5a-14cb-4c7c-a0ea-5013482a3d3e)


In the man page I found "-p" to specify the port. Looking at how the syntax should be like this:

ssh bandit0@bandit.labs.overthewire.org -p 2220

I was then prompted for a password for which I put bandit0. 

![image](https://github.com/reickcs/overthewire/assets/119334123/444aca42-7187-4007-8d81-9f77207952de)

I successfully gained access to the first level. 

![image](https://github.com/reickcs/overthewire/assets/119334123/a630a3ef-e9ab-46e9-9b89-d507554916d4)


## Bandit 0

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

## Bandit 1

Before moving on to the next level, I needed to leave my current machine. I used exit to leave the terminal. 

![image](https://github.com/reickcs/overthewire/assets/119334123/a5a2e60e-4692-45e4-a46e-2ceb8300c625)

I then used the instructions to move to the next level with this command.

ssh bandit1@bandit.labs.overthewire.org -p 2220

Through use of google I also found out that the command sequence in linux to paste in terminal is "Ctrl" + "Shift" + "V", to copy content in terminal it is "Ctrl" + "Shift" + "C"

![image](https://github.com/reickcs/overthewire/assets/119334123/91ef1742-845b-401e-aa4b-3377c28355bb)

Once inputing the password I was logged into bandit 1. 

The password is in a filed called - located in the home directory. I know that I am already in my home directory and when I use ls I see the file -. However, when I use cat - nothing happens. I learned that using cat - redirects to stdin, so the terminal was expecting input, but that was not my goals. I learned this from one of the resources provided on the overthewire page. 

![image](https://github.com/reickcs/overthewire/assets/119334123/f0f78e63-c2de-44f1-b314-ced7f026519a)

![image](https://github.com/reickcs/overthewire/assets/119334123/4951e188-2777-47d8-be41-b2bbe02f7c50)

I then added the full directory listing to specifiy exactly that it was a file and not expecting stdin. 

the command I used was "cat ./-"

The . specifies the current working directory, the / identifies I am looking for something in that directory, in this case I am in the home directory and looking for -

- <details><summary>The password is:</summary>
  <pre>
  rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
  </pre>
  </details>

