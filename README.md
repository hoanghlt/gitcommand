# Git Command
# Lệnh GIT mức độ cơ bản

## git config
Git config là câu lệnh mà chúng ta phải thực thi đầu tiên cài đặt git lên máy. Câu lệnh này sẽ giúp các bạn thiết lập tên và email cá nhân của bạn, những thông tin này sẽ đính kèm trong mọi commit của bạn, đều này sẽ rất hữu ích khi chúng ta muốn biết đoạn code nào đó đã được ai triển khai để có thể thảo luận trong trường hợp chúng ta không hiểu rõ đoạn code đấy sử dụng cho mục đích gì.

$ git config --global user.name "Your name"  
$ git config --global user.email "Your email
## git version
Nhìn vào câu lệnh chắc hẵn chúng ta cũng đoán ra được câu lệnh này dùng để kiểm tra phiên bản git đang sử dụng trên máy.

 $ git version
## git init
Đây là câu lệnh đầu tiên khi chúng ta bắt đầu một dự án mới, câu lệnh này sẽ giúp chúng ta tạo một repository mới, sau đó nó sẽ được sử dụng để lưu trữ và quản lý mã nguồn trong repository này.

$ git init 
// Hoặc bạn có thể đặt tên cho repo với lệnh
$ git init <your repository name>
## git clone
Câu lệnh này sẽ giúp chúng ta download một repository đã tồn tại sẵn trên khô lưu trữu (github, gitlab v.v) về máy.

git clone <your project URL>
## git add
Git add là câu lệnh giúp chúng ta thêm tất cả các file code mới mới hoặc các file code được chỉnh sửa vào repository.

$ git add your_file_name - Thêm một file( thêm mới hoặc chỉnh sửa) vào staging area
$ git add * - Thêm tất cả các file (thêm mới hoặc chỉnh sửa) vào staging area
## git commit
Đây là câu lệnh được sử dụng phổ biến nhất, câu lệnh này sẽ giúp chúng ta lưu các thay đổi ở các file trong vùng staging area xuống repository.

Có thể hiểu git add dùng để thêm thêm các file được thay đổi hoặc thêm mới vào vùng staging area, và chúng sẽ sẵn sàng để commit và sau đó những thay đổi này sẽ được lưu xuống repository.

$ git commit -m “your useful commit message”
## git status
Câu lệnh này cho phép bạn xem tình trạng hiện tại của mã nguồn như có bao nhiêu file được thêm mới hoặc chỉnh sửa.  Những file nào đang nằm trong vùng staging area hoặc đang nằm ngoài staging area.

## git branch
Trong một Git repository luôn luôn tồn tại nhiều nhánh riêng biệt dùng để triển khai một tính năng nào đó độc lập với các nhánh khác.

Các lệnh branch các bạn có thể sử dụng:

$ git branch
Dùng để hiển thị tất cả các branch đang có.

$ git branch
Dùng để tạo một branch mới.

$ git branch -d <branch_name>
Xoá branch.

## git checkout
Để di chuyển qua lại giữa các branch, chúng ta có thể sử dụng git checkout để đạt được điều này.

git checkout <branch_name>
Ngoài ra các bạn có thể vừa chuyển qua một branch mới và tiện thể khởi tạo nếu chưa tồn tại với câu lệnh.

 $ git checkout -b <your_new_branch_name>
Lệnh GIT mức độ trung bình
Sau các lệnh GIT cơ bản thường xuyên được sử dụng, chúng ta sẽ tìm hiểu các lệnh ở mức độ trung bình, cường độ sử dụng ích hơn.

## git remote
Repository được các bạn khởi tạo với câu lệnh git init chỉ đang tồn tại trên máy local của các bạn. Nếu muốn lưu trữ repository này lên một dich vụ lưu trữu git từ xa nào đó chẳng hạn như gitlab, github thì các bạn cần phải sử dụng git remote để kết nối giữa chúng.

$ git remote add <shortname> <url>
Ví dụ 

$ git remote add origin https://dev.azure.com/aCompiler/_git/DemoProject
## git push
Khi đã kết nối giữa local và dịch vụ lưu trữ git, chúng ta cần sử dụng lệnh git push để đồng bộ những thay đổi được commit trên local lên dich vụ lưu trữ.

$ git push -u <short_name> <your_branch_name>
Ví dụ
$ git push -u origin feature_branch
Ngoài ra trước khi sử dụng git push các bạn nên cấu hình origin và upstream.

$ git push --set-upstream <short_name> <branch_name>
Ví dụ
$ git push --set-upstream origin feature_branch
## git fetch
Git được sử dụng để làm việc nhóm, quản lý mã nguồn. Ngoài những commit của bạn thì còn vô số commit khác của các thành viên khác trong team. Sử dụng git fetch sẽ giúp chúng ta cập nhật tất cả những thông tin mới như commit, branch, v.v.

$ git fetch 
## git pull
Câu lệnh này sẽ download tất cả những nội dung (không chỉ là metadata như git fetch) từ dịch vụ lưu trữ xuống local repository.

$ git pull <remote_url>
## git stash
Git stash cho phép chúng ta lưu trữ các file được chỉnh sửa trong vùng nhớ tạm.

$ git stash 
Nếu muốn xem tất cả các stash các bạn có thể sử dụng lệnh

$ git stash list 
Nếu bạn muốn áp dụng các chỉnh sửa trong một stash nào đó lên branch hiện tại đang sử dụng.

$ git stash apply 
or 
$ git stash pop
## git log
Với câu lệnh git log các bạn có thể xem tất cả những commit trước đó được sắp xếp theo thứ tự commit gần nhất cho đến những commit cũ hơn.

$ git log 
## git shortlog
Nếu chỉ muốn xem git log với nội dung được tóm tắt ngắn gọn thì các bạn có thể sử dụng git shortlog.

$ git shortlog  
## git show
Lệnh này dùng để xem thông tin chi tiết của một commit bất kỳ.

$ git show <your_commit_hash>
## git rm
Đôi lúc các bạn muốn xoá một file từ code base, trong trường hợp này các bạn có thể sử dụng git rm.

$ git rm <your_file_name>
## git merge
Git merge cho phép các bạn kết mã nguồn và những thay đổi trên một branch khác vào branch hiện tại.

$ git merge <branch_name>
Câu lệnh này sẽ kết hợp những thay đổi trên branch có tên là <branch_name> vào branch hiện tại.

# Lệnh GIT mức độ nâng cao
Những câu lệnh ở mức độ nâng cao thường ít được sử dụng, và yêu cầu các bạn phải có kiến thức đủ tốt về git trước khi sử dụng. Và hãy sử dụng chúng thật cẩn thận nhé.

## git rebase
Git rebase tương tự như git merge, nó sẽ kết hợp 1 branch vào branch hiện tại với một ngoại lệ, git rebase sẽ ghi lại tất cả các lịch sử commit.

Bạn nên sử dụng lệnh Git rebase khi bạn có nhiều branch riêng dùng để hợp nhất thành một branch duy nhất. Và nó sẽ làm cho lịch sử commit trở nên tuyến tính và dễ truy vết hơn.

$ git rebase <base>
## git bisect
Git bitsect giúp bạn tìm ra những bad commit.

Để bắt đầu sử dụng 
$ git bisect start
Cho git bisect biết về một commit tốt
$ git bisect good a123
Cho git bisect biết về một commit xấu
$ git bisect bad z123
## git cherry-pick
Git cherry-pick là một lệnh hữu ích. Đó là một lệnhcho phép bạn chọn bất kỳ commit nào từ một branch bất kỳ và áp dụng nó vào một branch hiện tại.

$ git cherry-pick <commit-hash>
## git archive
Lệnh Git archive sẽ kết hợp nhiều tệp thành một tệp duy nhất. Nó giống như một tiện ích zip, vì vậy nó có nghĩa là bạn có thể giải nén các tệp lưu trữ để lấy các tệp riêng lẻ.

$ git archive --format zip HEAD > archive-HEAD.zip
## git pull –rebase
Nếu bạn muốn download content từ dịch vụ lưu trữ và dùng rebase thay vì merge thì có thể sử dụng

$ git pull --rebase
## git blame
Nếu bạn cần kiểm tra nội dung của bất kỳ tệp nào, bạn cần sử dụng git blame. Nó giúp bạn xác định ai đã thực hiện các thay đổi đối với tệp.

$ git blame <your_file_name
## git tag
Trong Git, các thẻ tag rất hữu ích và bạn có thể sử dụng chúng để quản lý bản phát hành. Bạn có thể coi thẻ Git giống như một nhánh sẽ không thay đổi. Nó quan trọng hơn đáng kể nếu bạn đang phát hành công khai.

$ git tag -a v1.0.0
## git verify-commit
Lệnh git verify-commit sẽ kiểm tra chữ ký gpg. GPG hoặc “GNU Privacy Guard” là công cụ được sử dụng trong các tệp ký tên và chứa các chữ ký của chúng.

$ git verify-commit <commit>
## git verify-tag
Tương tự git verify commit, các bạn có thể kiểm tra trên tag với lệnh

$ git verify-tag <tag>
## git diff
Nếu các bạn muốn so sánh một file code nào thay đổi những gì trước khi commit thì các bạn có thể sử dụng

$ git diff HEAD <filename>
Để kiểm tra sự khác nhau giữa mã nguồn hiện tại đã được thay đổi so với local repo
$ git diff HEAD <filename>
So sánh 2 branch
## git citool
Git citool là một giải pháp thay thế đồ họa của Git commit.

$ git citool
## git mv
Đổi tên git file từ tên cũ sang tên mới.s

$ git mv <old-file-name> <new-file-name>
## git clean
Bạn có thể xoá sạch các nội dung được thay đổi với các untracked files (chưa được theo dõi) với lệnh git clean.

$ git clean
## git help
Giúp bạn xem tất cả các thông tin cần thiết để sử dụng git.

$ git help <git_command>
## git whatchanged
Lệnh này thực hiện tương tự như git log nhưng ở dạng thô. Và đó là do nguyên nhân lịch sử.

$ git whatchanged

# gitcommand

II. Config
1. Short commands
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.st 'status -s '

Linux:
Config file’s location: ~/.gitconfig

Windows:
Config file’s location: C:\Users\{your_name}\.gitconfig

git config --global user.email "your_email@example.com"
git config --global user.username"lcdung"

git version

2. Remember username and password when using [http]
git config --global credential.helper cache
git config credential.helper cache

3. Ignore files
Edit file .gitignore

git update-index --assume-unchanged
git update-index --no-assume-unchanged

III. Basic commands
Mô hình Git 
1. Remote:
Mặc định (origin repository trên server và local repository trên local)

1. Add remote
  git remote add <remote_name> <url>
  
2. Checking name of current remote
  git remote -v
  View existing remotes
    origin  https://github.com/user/repo.git (fetch)
    origin  https://github.com/user/repo.git (push)

3. Rename remote
  git remote rename <old_name> <new_name>

4. Set URL remote
  git remote set-url origin https://github.com/user/repo2.git
  Change the 'origin' remote's URL

5. Delete
  git remote rm <remote_name>
  
2. Add files
1. Add multi files

git add <file1> <file2> ....
2. Add all files

Only adding modified files and new files
git add .

Adding all (deleted, modified and new)
git add --all
3. Pull
git pull
git pull <remote_name> <branch_name>
4. Push
git push <remote_name> <branch_name>

Force update
git push -f <remote_name> <branch_name>
5. Fetch
Update remote without deleting branches
git fetch <remote_name>

Update remote and deleting branch (if have)
git fetch <remote_name> --prune

IV. Main commands
1. Init
  Đây là câu lệnh đầu tiên khi chúng ta bắt đầu một dự án mới, câu lệnh này sẽ giúp chúng ta tạo một repository mới, sau đó nó sẽ được sử dụng để lưu trữ và quản lý mã nguồn trong repository này.
    git init

    git init <your repository name>

2. Clone
Câu lệnh này sẽ giúp chúng ta download một repository đã tồn tại sẵn trên khô lưu trữu (github, gitlab v.v) về máy.
    git clone <your project URL>

Clone single branch of repo:
git clone -b <branch_name> <url> {folder_name}
3. Status
git status
git status -s
4. Branch
List all branch of local:
git branch

List all branch of local and remote:
git branch --all

Create new branch and does not switch to new branch
git branch <new_branch>

Create new branch and switch to new branch
git checkout -b <new_branch>

Rename current branch to new_branch_name
git branch -m new_branch_name

Delete branch on local
git branch -D <branch_name1> <branch_name2> ...

Delete branch on remote
git push origin :<branch_name1> :<branch_name2> ...
git push origin --delete <branch_name1> <branch_name2>
5. Add files
Add multi files
git add <file1> <file2> ....

Git add là câu lệnh giúp chúng ta thêm tất cả các file code mới mới hoặc các file code được chỉnh sửa vào repository.

$ git add your_file_name - Thêm một file( thêm mới hoặc chỉnh sửa) vào staging area
$ git add * - Thêm tất cả các file (thêm mới hoặc chỉnh sửa) vào staging area

Add all files
Only adding modified files and new files
git add .

Adding all (deleted, modified and new)
git add --all
6. Commit
Commit a message
git commit -m "Sample message"

Edit commit message of last commit
git commit --amend -m "Edit sample message"
7. Logs
View short logs:
git log --oneline -10

View pretty logs:
git log --oneline --decorate --all --graph
8. Checkout
Checkout to branch
git checkout <branch_name>

Checkout to commit hash
git checkout <commit_hash>

Checkout file with commit hash
git checkout <commit_hash> <file_path>

Checkout file from another branch
git checkout <branch_name> <file_path>
9. Reset
Reset HEAD
git reset --hard
git reset origin/master --hard

Reset with commit hash
git reset <commit_hash>
10. Revert
Revert with commit hash
git revert <commit_hash>
11. Merge
git merge <branch_name>
12. Rebase
Để tích hợp các thay đổi từ nhánh này vào nhánh khác và commit trong nhánh hiện tại. (https://git-scm.com/book/vi/v1/Ph%C3%A2n-Nh%C3%A1nh-Trong-Git-Rebasing)

Rebase on branch: When rebase other brach need checkout other branch.

Rebase <branch_name> into current branch
git rebase <branch_name>

Rebase <branch_name2> into <branch_name1>
git rebase <branch_name1> <branch_name2>
Rebase on commit: When rebase other brach need checkout other branch.

git rebase -i <commit_hash>
  
Commands:
  p, pick = use commit
  r, reword = use commit, but edit the commit message
  e, edit = use commit, but stop for amending
  s, squash = use commit, but meld into previous commit
  f, fixup = like "squash", but discard this commit's log message
  x, exec = run command (the rest of the line) using shell

 These lines can be re-ordered; they are executed from top to bottom.

 If you remove a line here THAT COMMIT WILL BE LOST.

 However, if you remove everything, the rebase will be aborted.

 Note that empty commits are commented out
13. Cherry-pick
lấy commit từ branch khác về branch hiện tại.

git cherry-pick <commit_hash1> <commit_hash2> ..
14. Diff
So sánh code

 Diff two commit:
git diff <commit_hash1> <commit_hash2>

 Diff two branches:
git diff <branch_name1> <branch_name2>

 Diff file on two branches:
git diff <branch_name1> <branch_name2> -- <file_path>
15. Stash
Backup hiện trạng đang làm và nhảy code về bất kỳ version được backup trước đó.

 Stashed all changed
git stash

 List all stash
git stash list

 Show detail a stash
git stash show stash@{0}

 Apply latest stash to current branch
git stash pop

 Apply stash{0} into current branch
git stash pop stash@{0}

 Apply stash{0} into current branch
git stash apply stash@{0}

 Drop stash{0} into current branch
git stash drop stash@{0}

 Clear all stash
git stash clear
V. Tips & Notes
List all ignore files:

git ls-files -v | grep '^h'
Count modified files:

git status | grep 'modified:' | wc -l
Ignore chmod file:

git config core.fileMode false
Some commands need to push with option -f:

reset
rebase
commit --amend
