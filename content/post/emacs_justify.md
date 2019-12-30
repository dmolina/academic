+++
title = "Fill-more or the important of reading documentation"
author = ["Daniel Molina"]
date = 2017-12-15T11:28:00+01:00
lastmod = 2017-12-19T17:50:04+01:00
tags = ["emacs", "trick"]
categories = ["emacs"]
draft = false
+++

I **love** Emacs and the auto-fill more. When I work I use it always to make
easier to read the text (with a small value, like 80 or 100). Then, if I have
to copy to a Word Document (in collaboration with other people) or a text (like
in the submission of a review) I simple set the fill-column to a large value
(2000 or similar), with C-x f. Later, I copy all the text.

Until now I have suffered in silence a small problem in text-mode (not in
org-mode). If you put

```sh
Text.

- Item 1.
- Item 2.
```

After the fill-mode, you have:

```sh
Text.

- Item 1 Item 2.
```

And to have in right you have to put a line between them:

```sh
Text.

- Item 1.

- Item 2.
```

(The line between Text and first item is also required).

I though it was something inevitable, but checking the documentation,

<https://www.emacswiki.org/emacs/FillParagraph>

I have known that with a simple line in elisp that behavior is fixed:

```elisp
;; The original value is "\f\\|[      ]*$", so we add the bullets (-), (+), and (*).
;; There is no need for "^" as the regexp is matched at the beginning of line.
(setq paragraph-start "\f\\|[ \t]*$\\|[ \t]*[-+*] ")
```

I must check the available documentation more often :-).
