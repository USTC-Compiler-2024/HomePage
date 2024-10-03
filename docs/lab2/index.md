<!-- TODO: 
1）确定deadline
2）增加文档api介绍的内容
3）说明git仓库同步的流程，如何merge
4）在warmup阶段，有一些例子引用了仓库链接，需要同步仓库后更新这些链接！
 -->

# Lab2 中间代码生成

本次实验需要同学们在 Lab1 实现的 Cminusf 解析器基础上，完成从语法树向中间代码的自动化翻译过程。

## 实验内容

本次实验需要分阶段完成及验收。

### 阶段一

- 内容一：
  阅读 [Light IR 预热](./warmup.md)并参考 [Light IR 手册](./LightIR.md)，掌握手写 Light IR，使用 Light IR C++ 库生成 IR 的方法。
- 内容二：
  阅读[访问者模式](./visitor_pattern.md)，理解 C++ 访问者模式的工作原理及遍历顺序。

阶段一需要 **回答 [Light IR 预热](./warmup.md#思考题)与[访问者模式](./visitor_pattern.md#思考题)文档中的思考题**，回答内容保存为 `answer.pdf`。并完成 `tests/2-ir-gen/warmup/stu_ll` 与 `tests/2-ir-gen/warmup/stu_cpp` 目录下代码的编写。


!!! warning "Deadline"

    **2024 年 10 月 xx 日 23:59**

### 阶段二


阅读 [IR 自动化生成](./autogen.md)，[Cminusf 语义](./cminusf语义.md)，补充 `include/cminusfc/cminusf_builder.hpp` 与 `src/cminusfc/cminusf_builder.cpp` 文件，并通过 `tests/2-ir-gen/autogen/testcases/`目录下 `lv0_1`, `lv0_2`, `lv1` 级别的测试样例。

!!! warning "Deadline"

    **2024 年 10 月 xx 日 23:59**

### 阶段三

在阶段二的基础上，继续补充 `include/cminusfc/cminusf_builder.hpp` 与 `src/cminusfc/cminusf_builder.cpp` 文件，并通过 `tests/2-ir-gen/autogen/testcases/` 目录下所有提供的测试样例。

!!! warning "Deadline"

    **2024 年 10 月 xx 日 23:59**

## 实验要求

<!-- TODO:  -->

请将[实验仓库](https://cscourse.ustc.edu.cn/vdir/Gitlab/compiler_staff/2024ustc-jianmu-compiler)设置为上游仓库，并获取本次实验更新的内容，具体步骤如下：

将上游仓库设置一个别名（alias），在这里我们用 `upstream`，你也可以改成其他你喜欢的名字。在你 fork 后的本地仓库中：

```shell
$ git remote add upstream https://cscourse.ustc.edu.cn/vdir/Gitlab/compiler_staff/2023ustc-jianmu-compiler.git
```

尝试将远程的更新拉取到本地并进行 merge 操作：

```shell
$ git pull upstream master
```

当 merge 过程出现冲突时，请参考 [Lab0](../lab0/git.md#上下游同步和冲突处理) 来合理的解决冲突。

最后你需要将更改同步到你 fork 得到的远程仓库中：

```shell
$ git push origin master
```

## 提交内容

- 阶段一：在希冀平台提交你的 `answer.pdf` 文件，在希冀平台提交你实验仓库的 url（如 `https://cscourse.ustc.edu.cn/vdir/Gitlab/xxx/2023ustc-jianmu-compiler.git`）。
- 阶段二、三：在希冀平台提交你实验仓库的 url（如 `https://cscourse.ustc.edu.cn/vdir/Gitlab/xxx/2023ustc-jianmu-compiler.git`）。
