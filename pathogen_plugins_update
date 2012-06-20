#!/bin/bash
echo -e "\n\033[1mUpdating all vim plugin repositories...\033[0m"
cd ~/.vim/bundle
for dir in *
do
  echo -e "\n\033[1mUpdating $dir\033[0m"
  cd $dir
  if [ -d ".git" ]; then
    git pull
  elif [ -d ".hg" ]; then
    hg pull
  else
    echo -e "Plugin not under version control."
  fi
  cd ..
done
echo -e "\n\033[1mDone Updating.\033[0m"
