# OICPP IDE 官方文档

---

- $\text{by} \: \boxed{\texttt{linlin1195}}$

- 版本号：$\boxed{\texttt{v1.0.0\_beta3+001}}$，前缀与 OICPP 版本号一致，`+XXX` 表示文档修订。

- 本文档根据 [GPL 3.0](https://www.gnu.org/licenses/gpl-3.0.en.html) 开源，项目地址 `https://github.com/linlin1195/OICPP-Wiki`。

---

## 1 安装及更新

#### 1.1 下载及安装

要想下载 OICPP IDE，可以去它的官网 https://oicpp.mywwzh.top/  下载，也可以加入 QQ 群号 931577836，群文件里就有最新的版本。

下载后，打开并根据你的偏好安装，你的 OICPP 就诞生啦！

#### 1.2 更新

如果你在使用过程中遇到了 bug，或想尝试更多的功能，可以尝试升级版本或选择更稳定的版本（例如 beta 或 release 版本，下文有说明），那么我们如何更新版本呢？

1. 你可以点击上方菜单栏中的 "关于"—"检查更新"，程序检查到新版本后会下载安装包，之后一直点下一步即可安装。**（`v1.0.0_beta1` 以上版本目前无法通过此方法升级，请使用第二种方法）**
2. 如果下载不成功，你也可以从官网和群文件中下载安装包，并覆盖之前的安装目录，更新就完成了。

## 2 功能介绍

#### 2.1 编译运行

与 Dev-C++ 基本类似，选择编译器（见下）后 F9/F10/F11 或菜单栏 "运行"—"编译运行" 即可。

注意，当当前代码未编译直接运行时，要么出现警告，要么会运行上一次代码的结果。

#### 2.2 编译、编辑器设置

在 "关于"—"编译设置" 中可以自动下载 mingw 编译器，你也可以自己选择喜欢的编译器。

编辑器设置可以选择字母大小、字体等选项。

#### 2.3 模板设置

代码模板设置分为 文件模板 和 代码片段 两部分，文件模板会在新建文件时自动填充，而代码片段可以在编写时输入关键词（定义时设置）后添加。

#### 2.4 样例测试器

在左侧侧边栏中，类似 CPH，且支持 SPJ 与 testlib，填入输入和期望输出后运行即可，非常实用。

#### 2.5 代码对拍器

OICPP 提供了一个非常好用的对拍器，而无需文件输入输出，下面我们来看看怎么用。以下是一个实例。

比如说，我们要写一个输出 `a+b` 的程序如下：

```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
    int a,b;
    cin >> a >> b;
    cout << a+b << endl;
    return 0;
}
```

此为要对拍的代码。
然后是暴力文件：

```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
    int a,b;
    cin >> a >> b;
    for(int i=1;i<=b;i++){
        a++;
    }
    cout << a << endl;
    return 0;
}
```

最后是数据生成器：

```cpp
#include<bits/stdc++.h>
using namespace std;
const int MAXN = 1e8;
int main(){
    srand(time(0));
    cout << rand()%MAXN << " " << rand()%MAXN << endl;
    return 0;
}
```

之后选中即可。对拍组数上限 $10^5$，暴力文件运行速度不限。

#### 2.6 调试

与 Dev-C++ 相似，点击行号设置断电后调试即可。

#### 2.7 格式化代码

可使用快捷键 Alt + Shift + S 实现，详见下方 "快捷键" 。

#### 2.8 快捷键

| 键盘              | 效果     |
|:---------------:|:------:|
| Ctrl+N          | 添加文件   |
| Ctrl+S          | 保存文件   |
| Ctrl+滚轮         | 改变字母大小 |
| Alt + Shift + S | 格式化代码  |
| Ctrl+D          | 删除本行   |
| Ctrl+E          | 复制本行   |
| F9              | 编译     |
| F10             | 运行     |
| F11             | 编译+运行  |
| 更多的自己探索         | ……     |

## 3 bug 反馈

遇到了无法解决的 bug，你可以通过以下方式解决：

- 加入QQ群号 931577836，@群主 mywwzh 后说出你的问题。（但群主要改的bug太多了，可能来不及看。）
- 如果你有 GitHub，可以提 issues 反馈：https://github.com/mywwzh/oicpp-report/issues/new/choose

#### 3.1 日志

反馈 bug 前，请先查看日志，并将其和问题一并反馈，日志在 %userprofile%/.oicpp/logs。

#### 3.2 版本号说明

OICPP IDE 的版本号按字典序比较发布顺序，以下是一个标准的版本号。

```
v1.0.0_alpha1
```

其中前面的`v1.0.0`为功能版本号，有更新或很多 bug 修复时会迭代，`alpha1`为版本后缀，分为`alpha@`、`beta@`和`release@`。越往后越稳定，所以如果你想使用稳定的版本，当然是用`release`啦！（~~只不过还没有~~）
