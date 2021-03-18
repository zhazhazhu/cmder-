# CMDER笔记

## 查看当前目录绝对路径
pwd

## 查看当前目录内容
ls

## 查看指定目录内容
ls路径

## 查看文件内容
    cat 路径（全部展示内容）\
    head 路径（默认查看前10行，head 路径 -n 14，查看前14行）\
    tail 路径 （默认查看后10行，以上同理）\
    less 路径 （上下翻页，q结束）

    cd 路径 ：进入到指定路径

    cd ~/Desktop/  进入到桌面路径

## 清除屏幕
clear

## 创建空文件
touch 文件名（touch 1.txt）

## 同时创建多个文件
touch 文件名 文件名（touch 1.txt 2.txt）

## 创建文件和内容
echo 内容 > 文件名（echo nihao > 4.txt）

    追加内容：echo hi >> 4.txt
    echo -e  "hhhh\n888" >> 4.txt（同时创建多行代码，\n 表示回车）

    注意：一个大于号覆盖之前内容；两个大于号追加内容


## 创建文件夹
mkdir 文件名（同时创建多个文件夹：mkdir a b）

## 创建多层文件夹
mkdir -p 文件名/文件名/文件名

## 复制文件
cp 文件名 文件名

## 复制目录
cp -r 文件夹 文件夹

## 删除文件
rm 文件（rm 1.txt）

## 删除文件夹
rm -r 文件夹（rm -r a）

## 打开程序
start 文件（默认程序打开）

## 移动文件/文件夹
mv 文件 文件夹（mv 1.txt a      mv a/1.txt .）

## 重命名文件/文件夹
mv 1.txt 2.txt

## 修改文件最后的更新时间
touch 文件名

## 安装tldr程序
yarn global add tldr 或 npm i -g tldr

## 查看操作是否成功（echo $?）
成功返回0\
失败返回1\
；操作（不管成功或者失败都会执行后面操作）\
示例（rm 1.txt; echo 执行成功）\
重复上一个命令（alt+.）

## 多个命令一起配合（脚本）
### 在vscode里创建代码（abc变成可接受参数：$1）
```javascript
mkdir abc（$1）
cd abc（$1）
touch index.html
touch 1.js
touch 2.css
echo -e "<!DOCTYPE html><h1>标题</h1>" >>index.html
```
### 终端里创建代码(此时xxx为变量)
```javascript
进入到abc文件前一个目录
code abc(xxx)
chmod +x abc(xxx)
./abc(xxx)
```

