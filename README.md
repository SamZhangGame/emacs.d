# emacs.d
my configuration for emacs, scheme

based on
http://www.yinwang.org/blog-cn/2013/04/11/scheme-setup/
http://blog.csdn.net/luzheqi/article/details/17845009

reference
http://kelvinh.github.io/blog/2013/07/21/scheme-configuration-in-emacs/
http://www.cs.indiana.edu/chezscheme/emacs/
http://unschooled.org/2011/10/how-to-setup-emacs-for-clojure-on-mac-os-x-lion/

Usage From 王垠's blog http://www.yinwang.org/blog-cn/2013/04/11/scheme-setup/
ParEdit mode 的简单使用方法

ParEdit mode 是一个很特殊的模式。它起作用的时候，你不能直接修改括号。这样所有的括号都保持完整的匹配，不可能出现语法错误。但是这样有一个问题，如果你要把一块代码放进另一块代码，或者从里面拿出来，就不是很方便了。

为此，ParEdit mode 提供了几个非常高效的编辑方式。我平时只使用两个：
C-right: 也就是按住 Ctrl 再按右箭头。它的作用是让光标右边的括号，“吞掉”下一个S表达式。
比如，(a b c) (d e)。你把光标放在 (a b c) 里面，然后按 C-right。结果就是 (a b c (d e))。也就是把 (d e) 被整个“吞进”了 (a b c) 里面。

M-r: 去掉外层代码。
这在你需要去掉外层的 let 等结构的时候非常有用。比如，如果你的代码看起来是这样：
(let ([x 10])
  (* x 2))
当你把光标放在 (* x 2) 的最左边，然后按 M-r，结果就变成了
(* x 2)
也就是把外面的 (let ([x 10]) ...) 给“掀掉”了。
其它的一些按键虽然也有用，不过我觉得这两个是最有用的，甚至不可缺少的。有些其他的自动匹配括号的模式，没有提供这种按键，所以用起来很别扭。
