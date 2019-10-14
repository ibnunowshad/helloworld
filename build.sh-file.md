#!/bin/bash

#locale
folder=$1

#from git repo "git@gitlab.com:project-eva/nz-site.git" 
fromgiturl=$2
fromgitbranch=$3  #dev

#to main git repo git@gitlab.com:project-eva/us-region.git
togiturl=$4
togitbranch=$5  #zespriqa


echo "Hello, Zespri Kiwi!" $folder
echo Building..., $folder


# holds the number of arguments passed to the script
echo $# 

for arg in "$@"
do
    echo "$arg"
done
	

mkdir builtit #from
cd builtit

git init
git remote add origin $fromgiturl
git checkout -b $fromgitbranch
git pull origin $fromgitbranch  

npm install
npm run build 

mv build $folder  # rename folder

cp -avr $folder ../AMainRepo/build  #for backup in our local folder


#to
mkdir mainrepo 
cd mainrepo

git init
git remote add origin $togiturl
git checkout -b $togitbranch
git pull origin $togitbranch


#goto build folder and delete the existing build folder eg:en-US
cd build
rm -rf $folder 
cd ..  # go back to mainrepo folder



cd ..  # goto previous folder builtit
cp -avr ./$folder ./mainrepo/build  # copy locale folder to mainrepo build folder

cd mainrepo # again goback to mainrepo folder and run the below git push

git add .
git commit -m "push the $1 build"
git push origin $togitbranch


# To navigate to your home directory - go out of builit folder
cd .. # moving to builtit folder
cd .. # moving out of builtit folder


rm -rf builtit  #remove the builtit folder from our local computer
