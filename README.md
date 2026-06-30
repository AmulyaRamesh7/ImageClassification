 git clone https://github.com/AmulyaRamesh7/ImageClassification.git
  cd ImageClassification
 echo "original content">file.txt
$ git add .
$ git commit -m "initail commite"
$ git checkout -b feature
$ echo "feature added">file.txt
$ git add .
$ git commit -m "added feature"
$ git checkout main
$ echo "main branch content">file.txt
$ git add .
$ git commit -m "main change"
$ git merge feature
$ pwd
/c/Users/Amulya Ramesh/ImageClassification
$ git add file.txt
$ git commit -m "resolved merge conflict"
$ git checkout feature
$ git rebase main
