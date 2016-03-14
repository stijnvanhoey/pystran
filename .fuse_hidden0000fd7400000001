#!/usr/bin/env bash

# build the docs
cd docs
make clean
make html
cd ..

# commit and push
git add -A
git commit -m "building and pushing source docs"
git push origin master

# handle pages files
git checkout gh-pages 
# remove the old _files
rm -r ._*
# put new hmtl files in the directory
mv docs/build/html/* .

# commit the new docs for publishing
git add -A
git commit -m "publishing updated docs..."
git push origin gh-pages

# switch back
git checkout master
