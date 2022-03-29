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

Change binding key for some common/standard emacs:

```elisp
(progn
    (define-key evil-insert-state-map (kbd "C-a") 'mwim-beginning-of-code-or-line-or-comment)
    (define-key evil-insert-state-map (kbd "C-e") 'mwim-end-of-code-or-line)
    (define-key evil-insert-state-map (kbd "C-y") 'yank)
    (define-key evil-insert-state-map (kbd "C-k") 'sp-kill-hybrid-sexp)
    (define-key evil-insert-state-map (kbd "C-w") 'evil-delete)
    )
```

Note: the default for above change is below: 

```
C-a  evil-paste-last-insertion
C-e  evil-copy-from-below
C-y  evil-copy-from-above
C-k  evil-insert-digraph 
C-w  evil-delete-backward-word
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


## Biding Keys

Basic: 
* Key sequences are bound to cammnds in Emacs in various keymaps.
* The most basic map is the `global-map`
* Use `global-set-key` to update the global-map.
* Use `kbd` macro to define a key sequences with string.
* The global-map is often shadowed by other maps, e.g. `evil-mode`.

