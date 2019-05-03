# Middleman Project Bootstrapper Website

A bootstrapper for generating basic, static Middleman websites.

![Sample Website](https://i.imgur.com/OLwEw2G.png)

## Getting started

Start by ensuring you have ruby on your system. You **must** install [rbenv](https://github.com/rbenv/rbenv) to keep your ruby versions under control. Refer to rbenv's [installation guide](https://github.com/rbenv/rbenv#installation) on how to do so.

Ensure you have installed ruby version 2.3.1:

```bash
$ rbenv install 2.3.1
$ rbenv rehash
```

Then, install [bundler](http://bundler.io) to sort out your ruby dependencies:

```bash
$ gem install bundler
$ bundle install
```

#### El Capitan and OpenSSL issues

If you are using OS X El Capitan, install OpenSSL using `brew` and set the bundle
config to point to this install:

```bash
$ brew install openssl
$ bundle config build.eventmachine --with-cppflags="-I/usr/local/opt/openssl/include -L/usr/local/opt/openssl/lib"
```

## Changing MyProject to Your Project

Under a text editor of your choice, do a search and replace for `MyProject`. These are references for where you will need to replace MyProject to relevant content of your choice. The main pieces of data that need to ne changed are:

1. `data/global/footer.yml`
1. `data/landing_page.yml`
1. `source/layouts/index.html.erb`
1. `source/partials/_navbar.html.erb`
1. `source/articles/contributing/index.html.md.erb`
1. `source/articles/index.html.erb`
1. `source/articles/installation/{mac,ubuntu,windows}/index.html.erb`

You can also change theme colors and typography under `stylesheets/modules/_{colors,typography}.scss`.

## Developing

Develop using:

```bash
$ bundle exec middleman
```

Your website will be watched and hosted locally at **[http://localhost:4567/](http://localhost:4567/)**.

## Bootstrap

We currently rely on a [Ruby Bootstrap gem](https://github.com/twbs/bootstrap-rubygem/tree/v4.0.0.alpha4) compiled with Bootstrap 4.0.0-alpha4.
Relevant SASS files can be found [here](https://github.com/twbs/bootstrap-rubygem/tree/v4.0.0.alpha4/assets/stylesheets).

## Disclaimer

This bootstrapper was generalised from the [SplashKit](https://github.com/splashkit/splashkit.io) website. There may be some files lurking around that still reference SplashKit-specific details. You can ignore these.

## Publishing

Publish using:

```bash
$ rake publish
```

If this fails, try rebuilding the build folder from scratch then redeploy:

```bash
$ rm -rf build
$ rake publish
```

## License

Licensed under the MIT Licence.





------------------------------------------------------------------------------------------------------------------------


## Ontrack 

OnTrack is a web assessment tool that provides students with a task oriented approach to portfolio assessment to stay aligned by completing tasks as part of their learning. Students will work through a series of tasks in order to achieve a target grade to complete their unit learning outcomes.

OnTrack helps students to achieve their learning outcomes by taking the focus away from grades and placing the importance on learning of the content delivered by the unit. Grades will not be allocated for tasks during the course of their learning, instead, their learning will be assessed using the learning outcomes at the end of the unit.

The above will be achieved by the summative assessments completed at the end of the unit, by determining student grades with the evidence they present in their portfolio. The portfolio will consist of work that the student complete as part of tasks assigned in the unit. These tasks are designed in order to help students learn and demonstrate their achievements as part of learning outcomes of a unit.

## Create and Manage units

To get started with creating and managing a unit in OnTrack, ensure your account is of the correct permission level.

 1. Log in to OnTrack.
 2. Select Manage Units from the Administration dropdown in the top right menu.
 3. Select Create unit button at the bottom right corner.
 4. Enter the name and unit code of the unit.
 5. After the unit is created, select the newly created unit from the list of units.
 Now that the unit is created, there are a number of settings which must be populated before the unit can be properly used. Click on the link below for steps and more details:
 [Create and Manage units](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/unit_chair_guides/creating-and-managing-units/)

## Assign staff to a tutorial

Each tutorial in OnTrack should have an assigned teaching staff member, to ensure that the submissions for the tutorial are directed to the correct teaching staff.
To assign a tutor to a tutorial:

 1. Log in to OnTrack.
 2. Select Manage units from the Administration dropdown in the top right menu.
 3. Next, click on the appropriate unit to administer.
 4. Select the Staff tab to ensure that the tutor you wish to assign is enrolled in the unit, and has the correct permission.
 5. Once that is done, select the Tutorials tab, Select the tutorial in the list you wish to assign a tutor to.
 6. In the Tutor field, type the name of the appropriate tutor and select the tutor name from the dropdown.

 Need more help?[Click on me!](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/staff_guides/assign-teachers-to-a-tutorial/)

 ## Create and Manage users

 User accounts in OnTrack include both student and staff accounts. There are two ways to create user accounts, manually and batch.

**Edit an existing User**
 1. Log in to OnTrack.
 2. Select Manage Users from the Administration dropdown in the top right menu.
 3. To edit an existing user, select the user in the list, and this will open the Edit user modal.

 From this menu, you can edit the following fields:
    1.First Name
    2.Last Name
    3.Preferred Name
    4.Email
    5.Avatar
    6.System Role – Student | Tutor | Convenor/Unit Chair | Administrator.

**Create a New User**
From the Manage Users page, click the Add New User button on the bottom right to open the Create User modal.
This is identical to the edit user modal previously discussed, however, you can also set the username for the account.
Note: You cannot change the username.

**Batch Import/Export Users**
Users can be batch imported and exported by using a CSV file. To find the format of the CSV to be uploaded, you can click the download button in the users export panel to view the format, even if there are no users enrolled.

[Read more >>](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/staff_guides/create-and-manage-users/)

 ## Enrol and Manage students

 There are 4 options for administering students in units:

 1. Batch enroll or withdraw students
 2. Manually enroll or withdraw a student
 3. View and change student class allocations
 4. View student page

All of these actions take place in the student tab of the unit administration page.

 1. Log in to OnTrack.
 2. Select the Administer Units section.
 3. Click on the unit you are administering.
 4. Finally, select the Students tab.
 5. From the students page, you can perform the various student administration tasks. 

 [Read more >>](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/staff_guides/enrol-and-manage-students/)

## Create and Manage students in groups

To manage students in a group, first you need to ensure your unit has group sets setup.A group set is a definition of the types of groups you can have in a unit. 
Get started with the [setup](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/staff_guides/create-manage-student-groups/) for group set.

## Create and Manage students in tasks

Tasks are one of the most important aspects of running a unit in OnTrack. We will take a look at how we can create and manage tasks.

 1. Log in to OnTrack.
 2. Select Manage Units from the Administration dropdown.
 3. Select the unit you wish to administer.
 4. Select the Tasks tab.
 5. You will now see a list of tasks, or an empty panel if no tasks have been created in the unit.

 [Read more >>](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/staff_guides/creating-and-managing-tasks/)

 ## View and Interpret students and Task list

**Student List**
The student list is an important part of OnTrack, which shows all enrolled students in a unit, information such as student class allocation, and an overview of a student’s progression through a unit.

To view all student list,

 1. Log in to OnTrack.
 2. Select the unit from the Units You Teach list, then from the top-left menu, select Student List.
 3. You will see a list of students enrolled in the unit. The list is cut at 15 students per page, with pagination running across the bottom of the page. 
 4. By clicking anywhere in a list, you will be taken to the student’s profile page, which shows individual tasks status, their target grade, and burn down chart.

**Task List**
The task list simply lists each of the tasks in a unit. 
To view Task list

 1. Log in to OnTrack
 2. Select the unit from the Units You Teach list.
 3. Then, from the top-left menu, select Task List.
 4. It is broken down into three panels.
  
[Read more >>](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/staff_guides/viewing-class-information/)

## Grade student submissions  

Marking student submissions in Doubtfire is done throught the “Task Inbox” page. The Task Inbox is the default view after logging in to Doubtfire, and selecting a unit. 

[How is it done?](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/staff_guides/marking-tasks/)

## View and Analyse unit statistics

There are a number of different statistics available within the OnTrack, which can be viewed at any time during a unit by the teaching staff. We will explore how to view and interpret the different types of statistics. 
 1. To view all unit statistics:
 2. Log in to OnTrack.
 3. Select the unit from the Units You Teach list.
 4. From the top-left menu, select Unit Analytics.
 5. You will now be presented with the unit analytics page.
 
 [Read more >>](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/staff_guides/unit-statistics/)

## Glossary

This [Document](https://doubtfire-lms.github.io/doubtfire.io/articles/guides/tags/all_users/glossary/) contains a list of terms used throughout the Doubtfire system, explaining their meaning