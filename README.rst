Xblock RocketChat |build-status| |coverage-status| |codacy-status|
=========================================================

RocketChat Xblock allows to implement a chat window inside a course.

Installation
------------

Install the requirements into the Python virtual environment of your `edx-platform` installation by running the following command from the root folder:

```
$ pip install -r requirements.txt
```

Enabling in Studio
-------------------

After successful installation, you can activate this component for a
course following these steps:

* From the main page of a specific course, navigate to `Settings -> Advanced Settings` from the top menu.
* Check for the `Advanced Module List` policy key, and Add ``"rocketc"``` to the policy value list.
* Click the "Save changes" button.

Usage
-----
Include the RocketChat Xblock component in the content unit you want to control access to, and follow these steps on "settings":

* Select the condition to check.
* Enter the problem locator ids (as many as required) to evaluate the condition.
* Select an action to apply when the condition is met.


Common use cases
----------------

Flow Control can be used whenever you need to control the available course content based on grades obtained by a student, on one or more evaluated problems in the course. Also, it is possible to check if those problems have been answered or not.
Some common uses cases are:

* Only allow the learner to see unit B when a problem in unit A has been answered, otherwise displaying a explanatory message.
* Only allow the learner to see unit B when a problem in unit A has been answered, otherwise redirecting to unit A.
* Only allow the learner to see unit B when a problem in unit A has scored above a certain threshold.
* Present further explanatory content to learners that did not answer correctly a certain problem, while redirecting to the next unit learners that did answer correcly.
* Display a message congratulating the learner for passing an exam, or a message notifying the exam wasn't passed.
* Display a message notifying the learner that some of the exam's questions have not been answered yet.
* Used in combination with the subsection prerequites feature to better explain the learners why certain subsections will or will not be made available to them.


Features include
----------------

**Studio editable settings:** Allows to select the conditions and operators to evaluate and the actions to apply in a particular unit.

**Condition types:** Currently, the xblock features evaluating the score of a single problem and the average score of a list of problems.

**Condition operators:** The implemented operators are:

* Equals
* Not equal to
* Greather than
* Greather than or equal to
* Less than
* Less than or equal to
* Is empty
* Is not empty
* Has empty

**Actions:** This actions can be applied when a condition is met:

* Display a message
* Redirect to another unit in the same subsection (without reloading the page)
* Redirect to another unit using jump_to_id (reloading the page)
* Redirect to a given url

**WYSIWYG editor:** A simple to use HTML editor to simplify writing the content or message that learners will get if the condition is met.

About this xblock
-----------------

The RocketChat Xblock was built by `eduNEXT <https://www.edunext.co>`_, a company specialized in open edX development and open edX cloud services.



How to contribute
-----------------

* Fork this repository.
* Commit your changes on a new branch
* Make a pull request to the master branch
* Wait for the code review and merge process

.. |build-status| image:: https://circleci.com/gh/eduNEXT/rocket-chat-extension.svg?style=svg
   :target: https://circleci.com/gh/eduNEXT/rocket-chat-extension
   :alt: CircleCI build status
.. |coverage-status| image::  https://codecov.io/gh/eduNEXT/rocket-chat-extension/branch/master/graph/badge.svg
   :target: https://codecov.io/gh/eduNEXT/rocket-chat-extension
   :alt: Coverage badge
.. |codacy-status| image:: https://api.codacy.com/project/badge/Grade/31f24686b01944ac835ef835a6ce32bb
   :target: https://www.codacy.com/app/andrey-canon/rocket-chat-extension
   :alt: Codacy badge