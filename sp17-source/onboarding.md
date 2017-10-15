---
layout: page
title: Developing this Course
---

This is a quick guide on getting started on course development and management for Stat 140. If you have any questions beyond what's covered here, please contact Dibya. If you haven't already, create a Gitlab account [here](https://gitlab.com/), and send an email to Dibya with your username, asking to be added to the repo.


## Organization


The main center of course development is on GitLab under the organization **PROBABILITY**. You can access it at [https://gitlab.com/probability](https://gitlab.com/probability).

If you're correctly configured, you should see the following repositories

1. Internal Course Materials (gitlab.com/probability/course-materials) - The internal build system and beta course materials prior to release to students
2. Website (gitlab.com/probability/probability.gitlab.io) - The website source code for http://prob140.org
3. Textbook (gitlab.com/probability/textbook) - The textbook / lecture notes for this class: access the actual copy at http://probability.gitlab.io/textbook
4. Staging Textbook (gitlab.com/probability/textbook-staging) - The staged beta textbook: access the live version at http://probability.gitlab.io/textbook-staging
5. Assets (gitlab.com/probability/assets) - The live materials available to students - Used for Jupyter Interact
6. Explorations (gitlab.com/probability/explorations) - Some experiments and test-beds for problems and technologies before inclusion into the curriculum
7. Prob140 (gitlab.com/probability/prob140) - The repository for the `Prob140` library


## Workflow

### Course Materials

Course materials are homeworks, labs, and questions. Homeworks are weekly assignments composed of unrelated questions; they are released on Wednesday, and are due on Tuesday at midnight the following week. Labs are 2-hr long weekly assignment with some natural progression (or ultimate goal). Questions are small problems which are used to create homeworks. 

Course materials begin in the `course-materials` (Internal Course Materials) repository. To learn how to create a new homework or a new lab,  view the [README](https://gitlab.com/probability/course-materials/) in the `course-materials` repository. Once they have been designed and extensively tested, we will export the student code base from the `course-materials` repository, and place it into the `assets` repository. The student will now be able to click an *Interact* link, which will download the folder from the `assets` repository, and put it into their Jupyter server.

After the student has finished the assignment, they will use a library called `gsExport` to generate a PDF for use in Gradescope. This library segments the Jupyter notebook so it's easier to grade in Gradescope. Students will then submit this segmented PDF to gradescope, at which point grading happens. Once the deadline passes, the solution will be also be placed into the `assets` repository.

### Textbook

The textbook is a compilation of Markdown files and Jupyter Notebooks, all embedded in a GitBook.


### How The IPyNB parser works

In order for the iPython notebook parser to correctly go through your notebook, there are exactly three things that you have to follow:

1) When writing the notebook, remember to put "#SETUP" in cells that contain import code, "#SOLUTION" in cells that contains solutions (or where students should place solutions)

2) When writing doctests, remember to start the cell with "%%runDoctest", and put in all the doctests that you'd like following: Here's an example

	%%runDoctest
	>>> 1+1
	2
	>>> 10 == 2
	False

3) Remember to put `&zwnj;` in front of new questions and subquestions; this tells our Gradescope Exporter that a new question begins here, and to put the appropriate page break. Remember that the maximum difference between two `&zwnj;` is 2 pages, so if you think that the student will write more than 2 pages, be sure to insert more `&zwnj;` characters.

Here's an example of what this might look like (another really good guide is the starter notebook which is created when you make a new lab/question). All of these cells are markdown cells, by the way.

Cell 1

	&zwnj;
	## Subpart 1
	What is 1+1?

Cell 2

	#SOLUTION
	2

Cell 3

	&zwnj;
	## Subpart 2
	What is 1+2?

Cell 4

	#SOLUTION
	3	
