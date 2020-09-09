# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) SOFTWARE ENGINEERING IMMERSIVE

## Intro to Git

### Lesson Objectives

By the end of this lesson, you will be comfortable with:

- Utilizing git versioning to track changes to your code.
- Initializing a git repository.
- Staging and committing new and changed files in a git repository.
- Removing files from the staging area.

Ready to get started?

<p align="center">
  <a href="#">
    <img src="https://media3.giphy.com/media/Q5oq1gb4PK4ULDuiom/giphy.gif" alt="The Belchers" width="550px"/>
  </a>
</p>

<br>

### Why Git?

Git, at its core, is a _version control system_.

_Version control_ is the systematic process of tracking and storing multiple versions of a single project, allowing developers to merge and update projects in a collaborative (and safe) way.

As developers, our code is our livelihood. It's vital that we backup, edit, and contribute to code in a way that is safe, effective, and efficient.

This means that we need to edit our code in a way that...

- Doesn't break our live app (often referred to as "cowboy coding");
- Enables us to make changes in small, block-sized chunks.
- Tests our changes for unexpected conflicts or bugs;
- Documents our changes clearly and thoroughly, should we need to troubleshoot an update, or in the case of catastrophic mistakes, return to the prior versions; and

<br>

### But... why?

<details><summary>This is why.</summary>

![Alt Text](real-version-control.png)

</details>

There are a lot of advantages to version control, but namely:

- It decentralizes your code, making it easy to keep backups.
- It enables collaboration on complex code projects.
- it gives us the freedom to experiment and try new things without messing up the code base.

Ready to put this knowledge to use?

<br>

<p align="center">
  <a href="#">
    <img src="https://media0.giphy.com/media/SRxPbt5zLZXtMDhQUx/source.gif" alt="The Belchers" width="550px"/>
  </a>
</p>

***

### Code Along!

#### First, Create A Fresh Repo

- Make a directory, titled `bobs-burgers`.
- Drop into the bobs-burgers directory.
- Create a text file that we can version control with git, titled `bob`.

<details><summary>Reveal Commands</summary>

<details><summary>Are you sure? I bet you could recall it from memory.</summary>

<details><summary>Oh alright...</summary>

<br>

![Alt Text](https://media1.giphy.com/media/l2QDY7vkhfVYbCsEw/giphy.gif)

1. `mkdir bobs-burgers`
2. `cd bobs-burgers`
3. `touch bob.txt`

</details>
</details>
</details>

<br>

#### Next, Confirm Your Location & Files

(It's good to get in the habit...)

- Check your file path, if need be.
- Check which files you have in your current directory.
- Check the git status of your repository.

<details><summary>Reveal Commands</summary>

1. `pwd`
1. `l`
1. `git status`

_What happened?_

</details>

<br>

#### Initialize Your Git Repo

Of course, `git status` didn't help– this isn't a git repo yet.

- Initialize a git repo in this folder.
- Check which files are in the current directory again.

<details><summary>Reveal Commands</summary>

1. `git init`
1. `l`

_What changed?_

</details>

<br>

#### Finally, Let's Control Some Versions

- Add your `bob` file to your **git stage**.
- Check the git status of your repository again.
- Commit your staged file to **your working tree**.

One note about commit messages– clear and concise messages are imperative to collaboration. Follow Git commit message convention by using **the present-tense imperative**.

<details><summary>Reveal Commands</summary>

1. `git add bob.txt`
1. `git status`
1. `git commit -m "initialize git repo"`

</details>

<br>

<p align="center">
  <a href="#">
    <img src="https://media1.giphy.com/media/l0Hlx6jKwLPAd4PAc/source.gif" alt="The Belchers" width="550px" />
  </a>
</p>

You did it!

Git confirms that we've committed 1 file... _What else does it show in the message?_

<br>

***

### Staging & Committing

What just happened?

Once a repository is being tracked by git– once it's been **initialized–** all sub-folders and files can be in one of 3 **stages**:

1. `modified` means that you have changed the file in your working directory and saved it on your hard drive- but that's all.
1. `staged` means that you have _added_ a modified file– in its current version–
to be committed in your next commit.
1. `committed` means that the data is committed _to the working tree_ **in your local repository**.

Visually, it looks like this:

<p align="center">
  <a href="#">
    <img src="https://user-images.githubusercontent.com/6153182/33028677-839cda1e-cde4-11e7-83c5-59adf22958d9.png" alt="Stages" width="550px"/>
  </a>
</p>

<br>

***

### Code Along, Part 2

#### Let's Create Tina

1. Inside of the `bobs-burgers` directory, create a text file called `tina`.
2. Open the file with VS Code and copy in the following line:

<br>

<p align="center">
  <a href="#">
    <img src="https://media3.giphy.com/media/iyyKYEKuKTVpC/giphy.gif" alt="Tina" width="550px"/>
  </a>
</p>

<br>

```bash
"I have a photographic butt memory."
```

Then save the file.

#### Now, Add & Commit

1. Check the git status of the of the `bobs-burgers` directory. _What happened?_
1. Add her to the stage.
1. Commit her to the working tree.

<br>

***

### Review

#### Git Workflow Checklist

- [ ] `git status` to confirm clean working directory
- [ ] make changes to `<file-name>`
- [ ] `git add <file-name>`
- [ ] `git status` (to confirm modified files have been staged)
- [ ] `git commit`

<br>

#### Git Best Practices

- ALWAYS add files explicitly, if you can. If you have multiple files, use full paths to refer to each. Example: `git add foo/bar.md baz/qux.js`.
- ALWAYS use a commit message `git commit -m "an example commit message"`.
- ALWAYS use `git status` before any other command.
- NO commit is too small.
- NEVER, NEVER, NEVER mess with a git history. It is the cardinal sin of git. (`git reset` is safe, not affecting your history. For the purposes of this course, **do not use `git revert` or `git rebase`** on important code, like your projects.)

<br>

### Want more practice?

<details><summary>Self-Guided Learning</summary>

<br>

Let's keep going. Try to remember the commands- no worries if you can't, just refer to documentation!

#### Add Linda Belcher

Create a new text file called `linda`. Inside that file, write the following lines, then add and commit your changes:

```bash
"I've only had half of four bottles of wine."
```

Now that we've made our commit, let's see what happens when we type `git log`... _What does this return?_

This typically shows all of our previous commits, but since we just have one, that's all we see for now. Feel free to play around with flags for `git log`, like `--oneline`, `--name-status`, and `--graph`.

#### Remove Linda

Linda got tickets to the off-off-off Broadway dinner theater performance of Pirates of Penache. Let's remove her.

<br>

<p align="center">
  <a href="#">
    <img src="https://media1.tenor.com/images/73fe6fbbb94fc34f32406a8eacff78ab/tenor.gif?itemid=5383381" alt="Linda" width="550px" />
  </a>
</p>

<br>

Unstage the file with `git reset <"filename">`, then go back to your Bob's Burgers directory and remove it using `rm linda.txt`.

</details>

<br>

### This is all great, but one problem...

<br>

<p align="center">
  <a href="#">
    <img src="https://media2.giphy.com/media/3mJEuZtH6bcLpenJ3r/source.gif" alt="Tina" width="550px" />
  </a>
</p>

<br>

This has all taken place on your computer! What happens if your hard drive fails?

Let's move on to [Part 2: The GitHub Lesson](https://git.generalassemb.ly/sei-nyc-phoenix/github-lesson).

<br>

<p align="center">
  <a href="#">
    <img src="https://i.imgur.com/FTn4n1F.gif" alt="Tina" width="550px" />
  </a>
</p>