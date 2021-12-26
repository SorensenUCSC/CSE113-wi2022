---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: "Overview"
layout: single
classes: wide
---

## Class Description

Welcome to CSE 113: Parallel and Concurrent Programming! In this class we will explore many aspects of parallel computing, from instruction-level parallelism in seemingly sequential programs, to thread-level parallel programs that can efficiently execute across the many cores of today's multiprocessors. We will learn how to write programs that execute efficiently and correctly in concurrent environments. This class will give you the necessary foundation to solve problems using concurrency: a powerful skillset as today's computers are becoming more and more parallel.

## Necessary Background

The listed prerequisite classes are CSE 12 (systems), CSE 101 (data-structures and algorithms), and recommended CSE 120 (architecture). You will need some foundation in all of those topics to succeed in this class. In particular: parallel cooperative is often achieved through parallel data-structures, which have similar specifications and implementations to their sequential counterparts. We will discussing many aspects of the hardware/software interface, as such, you will need experience in a low-level programming lanaguage like C. Parallel programming is most efficiently executed on parallel hardware: Thus, you will need to understand shared resources (e.g. the memory hierarchy) of the underlying architectures. 

Because this is an upper division class, I do expect a general CS foundation. For the homeworks, I will assume that you are:

- comfortable using a linux command-line
- programming in a high-level language (e.g. Python)
- programming in a low-level language (e.g. C)
- a high-level understanding of computer architecture

## Class Modules

This class will be split into 5 modules, each of which are roughly two weeks:

* **Module 1: Introduction, Background and ILP** This module will introduce the class, provide an architectural refresher and discuss how modern hardware exploits parallelism within a thread (ILP).

* **Module 2: Mutual Exclusion** This module will discsuss the fundamental problem of mutual exclusion. We will discuss the theory behind mutual exclusion, how it is implemented in practice, and specialized mutual exclusion objects. 

* **Module 3: Concurrent Data Structures** This module will discuss concurrent objects and how to reason about them. We will discuss several implementations and conclude with a use-case about load balancing

* **Module 4: Reasoning about Concurrency** This module will discuss how to reason about concurrent programs, including memory consistency and fairness. 
 
* **Module 5: Heterogenous Parallelism (GPGPU)** This module will discuss heterogenous programming, with a focus on GPGPU programming. We will discuss the SIMT programming model, hierarchical execution, and different architectural considerations when optimizing programs.

## Class Format

Each class is 95 minutes. I will plan to have the zoom
room open 15 minutes before class starts and 15 minutes
afterwards. You can use this time to ask questions or socialize with
your classmates.

I will enable global chat for the zoom lectures. You may use this to
ask questions or comments throughout the lecture. The TAs will monitor the chat and ensure any questions or concerns are addressed. Peer-to-peer chat
will be disabled as it can be distracting.

_Non-protected materials_ will be hosted on this website. This
includes homework assignments, schedules, references, etc.

_Protected materials_ will be hosted on a Canvas website that you will
need your university credentials to access. These materials include
zoom links, lecture recordings, tests, grades, etc.

There will be an official forum in the Canvas that you can use to
discuss course topics and ask questions. At this time, I do not plan to host any other
official forum for the class (e.g. slack or discord). Feel free to
organize yourselves. If you do so, I only ask that you make an effort
to include all your classmates and adhere to academic integrity.

## Quiz/Attendence

This is special topics class, and as such, live discussions will be a
valuable part of the learning experience. I expect you to
make an effort to attend the live broadcast of this class on
zoom. **Attendance will be 10% of your grade**. I will upload
recordings of the class to canvas, but this is not a substitute for
attendance. Attendence will be taken through a small quiz given during the lecture.

Please message me if you will miss a lecture to avoid losing
attendance/quiz credit.

If the normally scheduled date and time will be an issue for you,
please let me know ASAP.

## Accessibility

UC Santa Cruz is committed to creating an academic environment that supports its diverse student body. If you are a student with a disability who requires accommodations to achieve equal access in this course, please submit your Accommodation Authorization Letter from the Disability Resource Center (DRC) to me by email, preferably within the first two weeks of the quarter. I would also like us to discuss ways we can ensure your full participation in the course. I encourage all students who may benefit from learning more about DRC services to contact DRC by phone at 831-459-2089 or by email at drc@ucsc.edu.

## Office Hours:

Between the instructor (Tyler) and the TAs, we will aim to have office hours _daily_. We have tried to spread them out between AM hours and PM hours to try and accomodate as many potential time zones as possible.

* Monday: TA office hour from 10:30 AM - 11:30 AM
* Tuesday: TA office hour from 10:30 AM - 11:30 AM
* Wednesday: Instructor office hour from 3:00 PM - 5:00 PM
* Thursday: TA office hour from 4:00 PM - 5:00 PM
* Friday: TA office hour from 3:00 PM - 4:00 PM

Zoom links can be found on Canvas

Please sign up for a 10 minute slot for office hours. The sign-up sheet can be found on Canvas. Please sign up for only 1 slot at a time. If there is no other student waiting at the end of your slot, you are welcome to stay. If you want to discuss an issue that you think others might also be interested in, please add the issue to the spreadsheet. If you see your issue listed, please add your name and we add more people to the discussion. 

The sign-up sheet is meant to provide fairness; as such I will be strict about keeping to the schedule. Please forgive any abruptness on my end.

_If you are in a different time zone that makes these hours difficult,
please message me and we can make accommodations_

## Asynchronous Communication

For any questions outside of office hours: first please consider posting the discussion forum on Canvas. If you have a question, there's a chance another student has the same question. If you have a private question, please email the teaching staff at: `cse113-spring21-teach-group@ucsc.edu`

This alias goes to the instructor and the TA. If you email any of us individually, we may kindly ask you to resend your email to the mailing list. If your question appears to be more appropriate for the discussion forum, we may kindly ask you to post your question there.

## Homework:

There will be one assignment per module (except for the last module), for a total of 4 homeworks.

We will host a docker container that includes the necessary environment (compilers, libraries) for the homeworks. You are free to run this docker from your local machine or from a unviversity machine. We will provide a list of university resources in Canvas.

The homeworks will be posted at least 2 weeks before they are due and can be found [here](homeworks.html).


## Tests:

There will be two asynchronous tests in this course: a midterm and a final. The
midterm will roughly be worth as much as a single homework assignment
(~10%). The final will be worth 30%

You will get the test as pdf worksheet and have 1 days to complete it. I
will design the tests to take ~120 minutes, a little longer than the time of a class. You
are free to consult notes, books, or the internet. While the test is active, you are not allowed to discuss the test with another person (either in the class or online). For example, you *can* google concepts that are on the test. You *cannot* post a test question to stackoverflow.

_a note on timing_: my tests are designed to take 120 minutes *if* they were given in-person. In practice, students take much longer on take-home tests because you can spend time validating answers and less time studying before hand. Because of this, many students spend much longer on take-home tests. Please consider this when budgeting time.

Please note our final is scheduled for Wednesday, June 9 from 4pm to 7pm.

## Late Policy:

Assignments are docked 5% per day late up to 4 days. After that they will no longer be accepted.  

The midterm is docked 20% per day late up to 4 days. After that, it will no longer be accepted.

The final will not be accepted late.

## Grade Breakdown

- Attendance/Quiz: 10%
- Homeworks: 50% (12.5% each)
- Midterm: 10%
- Final Exam: 30%

If you want to discuss a grade, please contact me no later than 1 week after the grades are posted.

## Academic Integrity

One of the joys of university life is socializing and working with your
classmates. I want you to make friends with each other and discuss the
material. 

**That said, I expect all assignments (homeworks, tests, paper
  reviews, presentations) to be your own original
  work.**

If you work together with a classmate on an assignment, please mention
this, e.g. in the comments of your code. If you use a figure you
didn't create in a presentation, then it needs a citation. Please
review the [universities policy on
plagiarism](https://guides.library.ucsc.edu/citesources/plagiarism)

This class has a zero tolerance policy on cheating. Please don't do
it. I would much rather get a hundred emails asking for help than have
to refer anyone for academic misconduct.

## Privacy

I want to include a quick note on Privacy. I will largely be using Zoom for remote lectures. You should be aware that:

- I will be recording lectures to host on Canvas for you to review. Things you do or say will be recorded. I doubt that this will be an issue, but if you want me to remove any part of the recording, please just let me know.
- Zoom chats are not private. Please be respectful and kind and assume everyone can see what you are typing.
- I will use best-practices to keep our Zoom lectures private to the class. Despite our best efforts, [Zoom has a checkered history w.r.t. privacy](https://www.theverge.com/2020/4/1/21202584/zoom-security-privacy-issues-video-conferencing-software-coronavirus-demand-response). However, Zoom is the best tool we have available and these risks are simply part of the reality we must deal with.

## Acknowledgements

This page is based off of Professor [Lindsey Kuper](https://users.soe.ucsc.edu/~lkuper/)'s CSE232, Fall 2020 website
