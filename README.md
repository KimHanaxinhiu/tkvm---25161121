mkdir demo-git
cd demo-git
git init

# 2. feat: thêm file code mới
echo 'console.log("Hello world!");' > hello.js
git add hello.js
git commit -m "feat: thêm file hello.js in ra Hello world"

# 3. docs: thêm README.md
echo "# Demo Git Commit" > README.md
echo "Project này để thực hành commit với feat, docs, fix." >> README.md
git add README.md
git commit -m "docs: thêm README với mô tả project"

# 4. fix: sửa lỗi chính tả trong file hello.js
sed -i 's/Hello world/Hello, World/' hello.js 

git add hello.js
git commit -m "fix: sửa chính tả trong thông báo hello"

# 5. Kiểm tra lịch sử commit
git log --oneline
