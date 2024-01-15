# huma_danzi
emacs 的性能不太好，所以用虎码官方的常用单字挂接码表转了一份单字版的
## usage
```emacs-lisp
(use-package pyim
  :custom
  (default-input-method "pyim")
  :config
  (pyim-scheme-add
    '(hmdz
      :document
      "虎码单字"
      :class xingma
      :code-prefix "hmdz/"
      :first-chars "abcdefghijklmnopqrstuvwxyz"
      :rest-chars "abcdefghijklmnopqrstuvwxyz"
      :code-prefix-history ("_")
      :code-split-length 4
      :code-maximum-length 4))
  ;;----'默认码表'
  (pyim-default-scheme 'hmdz))
```

然后将hmdz.pyim加入pyim-dicts

可以使用pyim-dicts-manager，或：
```emacs-lisp
(add-to-list pyim-dcits
    '(:name "hmdz" :file "/path/to/hmdz.pyim"))
```
