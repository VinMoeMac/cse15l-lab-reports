# Lab Report 4

## Logging into ieng6 account
<img width="652" alt="image" src="https://github.com/VinMoeMac/cse15l-lab-reports/assets/130107058/0904b433-8536-49c6-be0a-3eccc1bd546d">

Logging into the account was as simple as opening the terminal and putting `ssh cs15lsp23km@ieng6.ucsd.edu<enter>` followed by entering my password and hitting `<enter>`

## Cloning the repo
<img width="498" alt="image" src="https://github.com/VinMoeMac/cse15l-lab-reports/assets/130107058/3d7bdbb7-2289-41e4-881f-36c1f6ba98b0">

To clone the repository that I forked I inputted `git clone https://github.com/VinMoeMac/lab7<enter>`

## Running test
<img width="350" alt="image" src="https://github.com/VinMoeMac/cse15l-lab-reports/assets/130107058/8134d845-b411-4b38-8443-73f38fe138c1">

To switch directors to that of the lab I inputted `cd lab7<enter>` and then ran the bash script with the input `bash test.sh<enter>`

## Opening vim
<img width="368" alt="image" src="https://github.com/VinMoeMac/cse15l-lab-reports/assets/130107058/53fb6f56-fe5a-4d11-83a9-1dbe334bddce">

To edit ListExamples.java from the terminal I inputted `vim ListExamples.java<enter>` which takes me to the next screenshot.

## Code before change
![Image](beforeindex1.png)

To get here I scrolled with the cursor and then used the cursor to click the `1` that I needed to change.

## Code after change
<img width="542" alt="image" src="https://github.com/VinMoeMac/cse15l-lab-reports/assets/130107058/fc9d91dc-d42a-4d19-88eb-fe350823835d">

To make the change seen I inputted `x` to delete the `1` and then entered insert mode with `i` and pressed `2` to insert the character as instructed. To go back to normal mode I hit `<esc>` then `:wq` to quit vim and save changes. 

## Running test post change

<img width="311" alt="image" src="https://github.com/VinMoeMac/cse15l-lab-reports/assets/130107058/c6bdbd6b-f58b-4ba7-869d-5a9dae93cb18">

To check the changes were successful I ran the bash script with the input `bash test.sh<enter>` and it confirmed that both tests passed

## Git Commands to change the repo
<img width="469" alt="image" src="https://github.com/VinMoeMac/cse15l-lab-reports/assets/130107058/a57fcdba-64c8-49c0-8ef3-aba372fe0208">

To commit and push the changes to my account I first had to add the changed java file with the command `git add ListExamples.java<enter>` and then to commit I inputted `git commit -m "Fix merge method"<enter>` and finally I used a final github push with `git push<enter>`

