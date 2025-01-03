# How to contribute to transformers?

Everyone is welcome to contribute, and we value everybody's contribution. Code
is thus not the only way to help the community. Answering questions, helping
others, reaching out and improving the documentations are immensely valuable to
the community.

It also helps us if you spread the word: reference the library from blog posts
on the awesome projects it made possible, shout out on Twitter every time it has
helped you, or simply star the repo to say "thank you".

## You can contribute in so many ways!

There are 4 ways you can contribute to transformers:
* Fixing outstanding issues with the existing code;
* Implementing new models;
* Contributing to the examples or to the documentation;
* Submitting issues related to bugs or desired new features.

*All are equally valuable to the community.*

## Submitting a new issue or feature request

Do your best to follow these guidelines when submitting an issue or a feature
request. It will make it easier for us to come back to you quickly and with good
feedback.

### Did you find a bug?

The transformers are robust and reliable thanks to the users who notify us of
the problems they encounter. So thank you for reporting an issue.

First, we would really appreciate it if you could **make sure the bug was not
already reported** (use the search bar on Github under Issues).

Did not find it? :( So we can act quickly on it, please follow these steps:

* Include your **OS type and version**, the versions of **Python**, **PyTorch** and
  **Tensorflow** when applicable;
* A short, self-contained, code snippet that allows us to reproduce the bug in
  less than 30s;
* Provide the *full* traceback if an exception is raised.

To get the OS and software versions, execute the following code and copy-paste
the output:

```
import platform; print("Platform", platform.platform())
import sys; print("Python", sys.version)
import torch; print("PyTorch", torch.__version__)
import tensorflow; print("Tensorflow", tensorflow.__version__)
```

### Do you want to implement a new model?

Awesome! Please provide the following information:

* Short description of the model and link to the paper;
* Link to the implementation if it is open-source;
* Link to the model weights if they are available.

If you are willing to contribute the model yourself, let us know so we can best
guide you.

We have added a **detailed guide and templates** to guide you in the process of adding a new model. You can find them in the [`templates`](./templates) folder.

### Do you want a new feature (that is not a model)?

A world-class feature request addresses the following points:

1. Motivation first:
  * Is it related to a problem/frustration with the library? If so, please explain
    why. Providing a code snippet that demonstrates the problem is best.
  * Is it related to something you would need for a project? We'd love to hear
    about it!
  * Is it something you worked on and think could benefit the community?
    Awesome! Tell us what problem it solved for you.
2. Write a *full paragraph* describing the feature;
3. Provide a **code snippet** that demonstrates its future use;
4. In case this is related to a paper, please attach a link;
5. Attach any additional information (drawings, screenshots, etc.) you think may help.

If your issue is well written we're already 80% of the way there by the time you
post it.

We have added **templates** to guide you in the process of adding a new example script for training or testing the models in the library. You can find them in the [`templates`](./templates) folder.

## Start contributing! (Pull Requests)

Before writing code, we strongly advise you to search through the exising PRs or
issues to make sure that nobody is already working on the same thing. If you are
unsure, it is always a good idea to open an issue to get some feedback.

You will need basic `git` proficiency to be able to contribute to
`transformers`. `git` is not the easiest tool to use but it has the greatest
manual. Type `git --help` in a shell and enjoy. If you prefer books, [Pro
Git](https://git-scm.com/book/en/v2) is a very good reference.

Follow these steps to start contributing:

1. Fork the [repository](https://github.com/huggingface/transformers) by
   clicking on the 'Fork' button on the repository's page. This creates a copy of the code
   under your github user account.
2. Clone your fork to your local disk, and add the base repository as a remote:
   
   ```bash
   $ git clone git@github.com:<your Github handle>/transformers.git
   $ cd transformers
   $ git remote add upstream git@github.com:huggingface/transformers.git
   ```

3. Create a new branch to hold your development changes:

   ```bash
   $ git checkout -b a-descriptive-name-for-my-changes
   ```
   
   **do not** work on the `master` branch.
   
4. Set up a development environment by running the following command in a virtual environment:

   ```bash
   $ pip install -r requirements-dev.txt
   ```

5. Develop the features on your branch. Add changed files using `git add` and
   then `git commit` to record your changes locally:
   
   ```bash
   $ git add modified_file.py
   $ git commit
   ```
   
   Please write [good commit
   messages](https://chris.beams.io/posts/git-commit/). It
   is a good idea to sync your copy of the code with the original repository
   regularly. This way you can quickly account for changes:
   
   ```bash
   $ git fetch upstream
   $ git rebase upstream/master
   ```
   
   Push the changes to your account using:
   
   ```bash
   $ git push -u origin a-descriptive-name-for-my-changes
   ```
   
6. Once you are satisfied (**and the checklist below is happy too**), go to the
   webpage of your fork on Github. Click on 'Pull request' to send your changes
   to the project maintainers for review.
   
7. It's ok if maintainers ask you for changes. It happens to core contributors
   too! So everyone can see the changes in the Pull request, work in your local
   branch and push the changes to your fork. They will automatically appear in
   the pull request.


### Checklist

1. The title of your pull request should be a summary of its contribution;
2. If your pull request adresses an issue, please mention the issue number in
   the pull request description to make sure they are linked (and people
   consulting the issue know you are working on it);
3. To indicate a work in progress please prefix the title with `[WIP]`. These
   are useful to avoid duplicated work, and to differentiate it from PRs ready
   to be merged;
4. Make sure pre-existing tests still pass;
5. Add high-coverage tests. No quality test, no merge;
6. All public methods must have informative doctrings;


### Style guide

For documentation strings, `transformers` follows the [google
style](https://google.github.io/styleguide/pyguide.html).

#### This guide was heavily inspired by the awesome [scikit-learn guide to contributing](https://github.com/scikit-learn/scikit-learn/blob/master/CONTRIBUTING.md)
