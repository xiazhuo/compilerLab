# C++实现的一个RISC-V编译器

本项目参考 [北京大学编译实践课程](https://pku-minic.github.io/online-doc/#/) 实现了一个基于 Makefile 的 SysY 编译器

## 使用方法

首先 clone 本仓库:

```sh
git clone https://github.com/xiazhuo/compilerLab.git
```

在 [compiler-dev](https://github.com/pku-minic/compiler-dev) 环境内, 进入仓库目录后执行 `make` 即可编译得到可执行文件 (默认位于 `build/compiler`):

```sh
cd compilerLab
make
```

自行编写一个简单的hello.c程序后可进行测试：

```sh
build/compiler -riscv hello.c -o hello.s
```



若要分别查看 lab1 - lab8 的内容，请在右上角找到本项目的历史提交。

研究了两三天，由于本人采用on the fly式的中间代码生成，没有自定义中间代码的数据结构，很难添加机器无关级的优化
虽然官方libKoopa提供了koopa_parse_from_string的接口，但是却不允许在其上进行修改，现在处在一种很尴尬的境地。
