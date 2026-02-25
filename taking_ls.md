Extracting the zip file "The Flag.zip", a folder "The Flag" appears. Inside the folder, another folder is found with the same name, which contains a pdf file "The Flag.pdf" that requires a password. Running the command
```bash
ls -la
```
inside the directory of the folder where the pdf file resides in, a hidden directory .ThePassword can be found. The directory can be entered with
```bash
cd .ThePassword
```
and running the first command again, a hidden txt file ThePassword.txt can be found that can be read with
```bash
cat ThePassword.txt
```
that reveals the password "Im The Flag". Entering this password for the "The Flag.pdf" file, the flag is revealed.
