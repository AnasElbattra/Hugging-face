`GIT LFS` is used to store large files in the repository. 

To install it, open `Git Bash` in the folder where you want to upload the files and run the following command:
```
git lfs install

git lfs track "*.csv"   # or the desired file extension

git lfs push --all origin main

git add .

git commit -m "Add large files"     # add commit message

git push -u origin main
```