# bash命令介绍
## bash命令的基本格式说明（语法）

命令的名称 [-选项] [参数]

## 命令的介绍
### 切换目录的命令
cd:  change directory
```shell
cd Desktop
// cd 要切换到的目录的路径
```

### 显示当前所在的目录
pwd: print work directory

### 显示当前目录下的内容
ls: list

选项： -a      All显示所有内容
选项： -l	   以列表形式显示

-al 可以同时使用两个选项  当然也可以 分开写  ls -a -l

drwxr-xr-x
第一个d表示的就是当前是一个目录，如果第一个是- 就是一个文件
后面的rwxr-xr-x分为三组来理解
第一组的rwx, r就是read，可读，w就是write，可写，x就是Execute，可执行，文件所有者的权限
第二组的r-x   中间的-表示w权限没有       是文件所有者所在的用户组的权限
第三组的r-x   是指其他的所有用户的权限


ls -选项 参数(你要显示哪个目录的内容就写那个目录的路径)
参数如果不写，则默认显示当前的目录的内容

### 清空屏幕
clear


### 创建文件
touch
```shell
touch 文件名（或者文件路径）
```

### 删除文件
rm

```shell
rm 文件名（文件路径）
```

如果要通过rm命令删除文件夹，则需要添加一个选项 -r
```shell
rm -r 文件夹名称（文件夹路径）
```


选项 -f 可以强制删除一些文件



删除文件夹还可以通过 rmdir 命令，但是这个命令只可以删空文件夹


### 创建文件夹
mkdir命令

mkdir 文件夹名称 或者文件夹路径


### 读取文件内容
cat  一次性展示文件中所有的内容
cat 文件名（文件路径）


less 可以分页展示文件  按空格或者回车可以进行翻页  方向键也可以用来操作
展示完毕之后可以通过q键退出


### echo
将指定的内容进行输出  默认输出到了屏幕上


### 输出重定向
> ： 可以将输出内容重定向到指定的位置  覆盖操做
echo 123 > 1.txt

>>: 追加操作

### 复制文件的操作
cp

cp 文件名 要复制成的文件名

### 移动文件的命令

mv

mv 文件名  目标位置

mv 可以用来做文件重命名的操作！