<!---

TASK LIST:

  * Use cp -rf *.* to copy all of the files and directories in this repository
    to the starter repository for this assignment
  * Change into the directory for the starer repository
  * Update the header (e.g., #) to only give the name of the assignment
  * Update the first paragraph to include the commented-out content
  * Change the link in the # Problems section to point to this lab's starter
  * Create the assignment in the GitHub Classroom, noting the URL
  * Test the assignment by accepting it with your own GitHub account
  * Check to ensure that your GitHub repository is created correctly
  * Share the assignment link with all of the students using email or Slack

PROBLEMS?

  * Contact Gregory M. Kapfhammer by email or Slack
  * Raise an issue in the GitHub repository for this assignment

-->

# cs100-F2018-lab9-starter

Designed for use with [GitHub Classroom](https://classroom.github.com/), this
repository contains the solution for Laboratory 9 in Computer Science 100.
Since the Travis builds for this repository will initially fail (as evidenced
by a red &#x2717; appearing in the commit logs instead of a green &#x2714;),
the programmer is responsible for completing all of the steps needed to satisfy
the requirements for the assignment, thus causing a &#x2714; to instead appear
in the commit logs.

## Introduction

This assignment requires programmers to test and improve a Java program, called
`TodoListManager`, that will produce textual output demonstrating the complete
management a list of tasks that must be finished. First, the program will
display a welcome message. Then, it will accept commands from the user and
repeatedly perform the requested operations. As verified by
[Checkstyle](https://github.com/checkstyle/checkstyle), the source code for the
`TodoListManager.java`, `TodoListItem.java`, and `TodoList.java` files must
adhere to all of the requirements in the [Google Java Style
Guide](https://google.github.io/styleguide/javaguide.html).

The programmer is also responsible for writing a one-paragraph reflection,
stored in the file `writing/reflection.md`, that explains the challenges that
they faced and the solutions they developed and their strategy for managing and
searching the list of tasks. This is a Markdown file that must adhere to the
standards described in the [Markdown Syntax
Guide](https://guides.github.com/features/mastering-markdown/). Remember, you
can preview the contents of a comitted Markdown file by clicking on the name of
the file in your GitHub repository. Finally, don't forget that your
`writing/reflection.md` file should adhere to the Markdown standards established
by the [Markdown linting tool](https://github.com/markdownlint/markdownlint) and
the writing standards set by the [Proselint tool](http://proselint.com/).

When you use the `git commit` command to transfer your source code to your
GitHub repository, [Travis CI](https://travis-ci.com/) will initialize a build
of your assignment, checking to see if it meets all of the requirements. If both
your source code and writing meet all of the established requirements, then you
will see a green &#x2714; in the listing of commits in GitHub. If your
submission does not meet the requirements, a red &#x2717; will appear instead.
The instructor will reduce a programmer's grade for this assignment if the red
&#x2717; appears on the last commit in GitHub immediately before the
assignment's due date.

A carefully formatted assignment sheet for this project provides more details
about the steps that a computer scientist should take to complete this
assignment. You can view this assignment sheet by visiting the listing of
laboratories on the course web site.

## Learning

If you have not done so already, please read all of the relevant [GitHub
Guides](https://guides.github.com/) that explain how to use many of the features
that GitHub provides. In particular, please make sure that you have read the
following GitHub guides: [Mastering
Markdown](https://guides.github.com/features/mastering-markdown/), [Hello
World](https://guides.github.com/activities/hello-world/), and [Documenting Your
Projects on GitHub](https://guides.github.com/features/wikis/). Each of these
guides will help you to understand how to use both [GitHub](http://github.com) and
[GitHub Classroom](https://classroom.github.com/).

To do well on this assignment, you should also review Chapters 1 through 4 and
study Sections 5.1 through 5.6. Please see the course instructor or one of the
teaching assistants or tutors if you have questions about any of these reading
assignments.

## Commands

To get started in using the GatorGrader tool, you can change into the directory
for this assignment and type the command `gradle grade` in your terminal.
Running this command will produce a lot of output that you should carefully
inspect. If the output indicates that GatorGrader judges that there are no
mistakes in the assignment, then this means that your source code and writing
are passing all of the automated baseline checks. However, if the output
indicates that there are mistakes, then you will need to understand what they
are and then try to fix them.

You can also complete several important Java programming tasks by using the
`gradle` tool. For instance, you can compile (i.e., create bytecode from the
program's source code if it is a correct program) the program using the command
`gradle build`. There are also additional commands that you can type:

* `gradle clean`: clean the project of all the derived files
* `gradle check`: check the quality of the code using Checkstyle
* `gradle build`: create the bytecode from the Java source code
* `gradle run`: run the Java program in the command-line
* `gradle tasks`: display details about the Gradle system

To run one of these commands, you must be in the main directory for this
assignment where the `build.gradle` file is located. Then, you can type the
command in the terminal and study the output. Please note that, since this
program interacts with the user in the terminal window, you must run it
differently than you ran past programs. Specifically, you should use the
following command to run the `TodoListManager`:

```
gradle -q --console plain run
```

## Checks

In addition to meeting all of the requirements outlined in the assignment
sheet, your submission must pass the following checks:

* labnine/TodListItem.java:
  * Features at least one single-line comments
  * Features at least fifteen multiple-line comments
  * Contains exactly zero uses of a `println(` statement
  * Contains exactly one use of a `new Date(` statement
  * Contains exactly zero uses of a marker for incomplete work

* labnine/TodoList.java:
  * Features at least fourteen single-line comments
  * Features at least eleven multiple-line comments
  * Contains at least five uses of a `while (` loop
  * Contains at least four uses of a `if (` statement
  * Contains at least six uses of a `ArrayList<TodoListItem>` statement
  * Contains at least seven uses of a `Iterator<TodoListItem>` statement
  * Contains exactly zero uses of a `println(` statement
  * Contains exactly zero uses of a marker for incomplete work
  * Runs correctly without crashing or producing an error
  * Produces exactly twelve lines of output in the terminal

* labnine/TodoListManager.java:
  * Features at least three single-line comments
  * Features at least two multiple-line comments
  * Contains at least three uses of a `while (` loop
  * Contains at least six uses of a `if (` statement
  * Contains at least five uses of a `else if (` statement
  * Contains at least ten uses of a `println(` statement
  * Contains exactly one uses of a `break` statement
  * Contains exactly zero uses of a marker for incomplete work
  * Runs correctly without crashing or producing an error
  * Produces exactly twelve lines of output in the terminal

* writing/reflection.md:
  * Passes the checks performed by the Markdown linting tool
  * Passes the checks performed by the proselint linting tool
  * Contains exactly one contiguous paragraphs of formatted text
  * The contiguous paragraph contains at least 100 words

* GitHub repository:
  * Contains five commits beyond the repository's starting number of commits

## Output

Using the provided file, the `TodoListManager` should read in items from a list
and then provide the opportunity to manipulate and search through that list. The
program should proceed iteratively, giving the user the ability to quit the
program and then displaying a closing message. A sample of the output that this
program could produce is provided below. Importantly, please ensure that you
test your program with different inputs than those that are provided in the
file. What are some other ways in which you think that it would be a good
idea to test this program?

```
Welcome to the Todo List Manager.
What operation would you like to perform?
Available options:read, priority-search, category-search, done, list, quit
read
list
0, A, Understand, Draw diagram(s) to explain classes, done? false
1, A, Understand, Use the LJV to see TodoList, done? false
2, B, Explain, Add comments to all of the Todo classes, done? false
priority-search
What is the priority?
A
0, A, Understand, Draw diagram(s) to explain classes, done? false
1, A, Understand, Use the LJV to see TodoList, done? false
category-search
What is the category?
Explain
2, B, Explain, Add comments to all of the Todo classes, done? false
done
What is the identifier of the task?
0
list
0, A, Understand, Draw diagram(s) to explain classes, done? true
1, A, Understand, Use the LJV to see TodoList, done? false
2, B, Explain, Add comments to all of the Todo classes, done? false
quit
Thank you for using the Todo List Manager.
```

## Updates

If the course instructor updates the provided material for this assignment and
you would like to receive these updates, then you can type this command in the
main directory for this assignment:

```
git remote add download git@github.com:Allegheny-Computer-Science-100-F2018/cs100-F2018-lab9-starter.git
```

You should only need to type this command once; typing the command additional
times may yield an error message but will not negatively influence the state of
your repository. Now, you are ready to download the updates provided by the
course instructor by typing:

```
git pull download master
```

This second command can be run whenever the course instructor needs to provide
you with new source code for this assignment. However, please note that, if you
have edited the files that the course instructor updated, running the previous
command may lead to Git merge conflicts. If this happens, you may need to
manually resolve them with the help of the instructor or a teaching assistant.

## Travis

This assignment uses [Travis CI](https://travis-ci.com/) to automatically run
the checking programs every time you commit to your GitHub repository. The
checking will start as soon as you have accepted the assignment, thus creating
your own private repository, and the course instructor enables Travis for it. If
you are using Travis for the first time, you will need to authorize Travis CI to
access the private repositories that you created on GitHub.

## Requirements

The GatorGrader software that supports the checking of this assignment was
developed for the following software and versions:

* Gradle 4.6
* Java 1.8.0
* MDL 0.4.0
* Proselint 0.8.0
* Python 3.6

## Problems

If you have found a problem with this assignment's provided source code, then
you can go to the [Computer Science 100 Lab 9
Starter](https://github.com/Allegheny-Computer-Science-100-F2018/cs100-F2018-lab9-starter)
repository and create an issue by clicking the "Issues" tab and then clicking
the green "New Issue" button. If you have found a problem with the [GatorGrader
tool](https://github.com/GatorEducator/gatorgrader) and the way that it checks you
assignment, then you can follow the aforementioned steps to create an issue in
its repository. To ensure that your issue is properly resolved, please provide
as many details as is possible about the problem that you experienced. If you
discover a problem with the laboratory assignment sheet, then please raise an
issue in the
[cs100-F2018-sheets](https://github.com/Allegheny-Computer-Science-100-F2018/cs100-F2018-sheets)
repository and mention this assignment.

Students who find, and use the appropriate GitHub issue tracker to correctly
document, a mistake in any aspect of this laboratory assignment will receive
free laptop stickers and extra credit towards their grade for it.

## Assistance

If you are having trouble completing any part of this project, then please talk
with either the course instructor or a teaching assistant during the laboratory
session. Alternatively, you may ask questions in the Slack workspace for this
course. Finally, you can schedule a meeting during the course instructor's
office hours.
