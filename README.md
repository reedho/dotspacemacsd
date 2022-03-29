# Change logs

## 29-Mar-2022

The following variable was set/updated: 

```
clojure-indent-style                   'align-arguments
clojure-align-forms-automatically      t
clojure-toplevel-inside-comment-form   t
dotspacemacs-scratch-buffer-persistent t
dotspacemacs-scratch-buffer-unkillable t
dotspacemacs-smartparens-strict-mode   t
dotspacemacs-smart-closing-parenthesis t
dotspacemacs-whitespace-cleanup        changed
undo-tree-auto-save-history            nil
```

# Configuration Info

## Clojure

Default `clojure-indent-style` is `always-align`, the other two options is
`always-indent` and `align-arguments`.

always-align:

```clojure
(reduce merge
        some-coll)
(reduce
 merge
 some-coll)
```

always-indent:

```clojure
(reduce merge
  some-coll)
(reduce
  merge
  some-coll)
```

align-arguments:

```clojure
(reduce merge
        some-coll)
(reduce
  merge
  some-coll)
```
