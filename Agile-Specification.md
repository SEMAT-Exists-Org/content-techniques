#TECHNIQUE
##Name
Agile Specification
##Type
Technique
##Author
Nick Strugnell, Red Hat 2016
##License
Creative Commons Attribution-ShareAlike 4.0
https://creativecommons.org/licenses/by-sa/4.0/
![CC BY SA](https://licensebuttons.net/l/by-sa/3.0/88x31.png)

----------
##Summary
A universal technique for gathering requirements that is the main way consulting projects scope, plan and organise project delivery based on a clear set of defined requirements

##Description
The TECHNIQUE :  Agile Specification is a universal technique used for gathering requirements for consulting projects. It can be used as a standalone technique to fulfil the ACTIVITY : Requirements Gathering or in concert with other technology-specific specification techniques. For further information on requirements gathering and specification techniques, refer to the ACTIVITY : Requirements Gathering

 

This technique uses elements of [Agile Software Development](https://en.wikipedia.org/wiki/Agile_software_development) to gather requirements in terms of User Stories. Individual user stories are broken down into tasks and estimates are made on the effort that will be required to implement each user story. In contrast with TECHNIQUE: System Requirements Specification which is a reductivist approach that attempts to completely specify the behaviour of the system before any development takes place, Agile Specification works on the assumption that not all requirements will be known at the onset of the project, and that requirements may change during delivery. This is in line with the principles of the [Agile Manifesto](http://agilemanifesto.org/principles.html). 

Although some stakeholders may be familiar with Agile, it is likely that the majority are not so it is incumbent on you to explain what the process will be and why we are taking this approach. A checklist for things to discuss includes:

 

   - What traditional requirements are - functional, non-functional, design etc.
   - What some of the problems with traditional requirements gathering are - fails to capture the big picture, does not easily adapt to change, requirements conflict
   - How Agile attempts to address this - capture requirements as User-focused stories, deliver working code early, iterative approach, requirements as an ongoing process rather than upfront
   - Explain how we want to gather enough requirements to have an overall picture of the work, and to start the work (e.g. enough for the 2-3 sprints) but that minutely specifying the work is not productive as requirements inevitably change during the delivery of any sufficiently large project as the problem becomes better understand

Finally, on the board demonstrate what a user story is. I tend to write up at the top of the board:

"As a `<role>` I want `<goal>` so that `<benefit>`"

 
###Discover User Stories

Elicit user stories going round the table, starting with the stakeholders who have the greatest vision of the project (e.g. the project sponsor) and working down to those with the narrowest vision (e.g. the security officer). Encourage conversation, and out-of-turn submission of user stories (e.g. "Oh, that reminds me, I just thought of..."), however any criticism of other stakeholders user stories should be cut off immediately - remind users that they will have a chance to discuss and rank each others user stories at a later point.

 

User stories will often vary wildly in their technical complexity and specificity. For example, a project sponsor may have:


"As an IT Manager, I want to have the ability to assign compute resource quotas to my endusers in order to reduce virtual machine sprawl."

 

whereas a Security Office may have:

 

"As a Security Office, I require that all systems we deploy be compliant with PCI DSS v3.0 in order to meet our regulatory requirements."


(Some of you may recognise the first user story as encapsulating a Functional Requirement while the second encapsulates a Design Requirement.

 

Typically, the more senior the staff, the more "big picture" the user stories, whereas more junior staff will generally have more technical user stories. All user stories that are missing either role, or benefit should be challenged. The following lists some valid user stories:-

- "As an end user, I want the ability to be able to request a virtual machine via a self-service web console rather than the existing spreadsheet based request form, so that I can quickly deploy VMs to satisfy business needs rather than waiting on the IT department to do it for me."
- "As an end user, I want to be able to log in to the self-service web console using my Active Directory username and password, so that we do not have to duplicate our directory and authentication systems"
- "As a system administrator, I want to be able to assign a quota of CPU, memory and disk to each department in my organisation, so that I can cross-charge them for the resources that they actually use."
- "As the IT Director, I need to ensure that all customised code developed by Red Hat Consulting will be fully supported by Red Hat Support in the future, so that I can assure my board that we are not running critical infrastructure on unsupported systems"

And the following user stories should be challenged:-

- "We need to be able to check who's logged into the web portal over the last 6 weeks"
- "I want to be able to suspend people's accounts if they leave the company"
- "If the system doesn't support us uploading VM requests via SOAP, it won't be any good for us"
- "Whatever the new system does, it shouldn't break the integration of the existing VMWare estate with our AD server"

While all these are potentially valid concerns, they can all be formulated as a user story.

User stories should be written on large post-its and stuck on the whiteboard - this enables everyone to see the current state of the process and helps them formulate their own user stories.

Carry on gathering user stories around the table until the pace of user story generation starts to slow down markedly - this might take two or three rounds of iteration of every person in the room. At this point you should make it clear that while you may have not gathered all user stories, you have gathered enough user stories to start the work. This is one of the key concepts of Agile - you now have enough to get the work started but fully expect further user stories to be generated during the delivery of the work, and for user stories to be changed as the problem being addressed becomes better understood.

Lastly, in software development it is usually required that user stories are independent ie each user story should be able to be implemented independently and not reliable on another user story being implemented beforehand. This requirement is not realistic with infrastructure projects which tend to be more linear and it should be considered normal to have at least some independence between user stories.

 
###Ranking

Ranking each user story in order of importance is a useful exercise to determine the real requirements for the project and to determine how much actual need there is for each user story, particularly ones that were created towards the end of the discovery stage. A simple method for ranking is as follows:

1. Jumble up the user story stickies on a board - it's important not to give any initial indications of rank
2. Taking each user story at random, go round the room and ask each stakeholder to assign a level of importance to the user story on a scale of 1 to 10, where 1 is the least important and 10 is the most.
3. Write the sum of the stakeholders ranking on each user story.
4. When finished, re-arrange the stickies into a ranking from most important to least important.
5. Have a brief discussion with the stakeholders on whether they would like to discard some lower ranked stories e.g. the latest 10%, reminding them that the nature of Agile development means that these can always be re-introduced in a later sprint if the requirement for them becomes more important.
 
###Technology Decisions and Task Drilldown

The next stage of requirements gathering is to make some technology decisions and drill down on the user stories you have gathered so far. The user stories should now be in rank order of importance and should be analysed in that order.

 

For each user story, three decisions need to be made:

1. What technology will be needed to implement this user story (it's valid at this stage to have alternate technologies - there's more than one way to do it!)
2. What tasks will need to be accomplished to implement this user story
3. What is the definition of done for this user story? (in other words, the acceptance criteria)

Use some smaller stickies for the technology, tasks (each task on a separate sticky) and defintion of done - I use green for technology, yellow for tasks and pink for definition of done.

 

###Example


**User Story**: "As an end user, I want the ability to be able to request a virtual machine via a self-service web console rather than the existing spreadsheet based request form, so that I can quickly deploy VMs to satisfy business needs rather than waiting on the IT department to do it for me."

**Technology**: Cloudforms or Openstack
**Task 1**: Development of user story test plan

**Task 2**: Initial Cloudforms management engine deployment and configuration

**Task 3**: Registration of virtualisation providers with CFME

**Task 4**: Creation of end users with correct roles to request deployment of machines

**Task 5**: Demonstration of successful deployment of virtual machine as end user (execution of test plan)

 

When performing the task drilldown, look for duplication of tasks across multiple user stories. For example, in the above example, Task 2, the initial deployment of CFME is likely to be a task replicated in other user stories. The duplicated tasks can be treated in two different ways:

 

1. Leave the duplicated tasks in just one user story and remove them from the others. With this approach, you will introduce multiple dependencies across user stories which can introduce problems at the delivery stage.
2. Collect all duplicated tasks into one or more 'Infrastructure and Architecture' user stories. These are user stories which must be implemented before the remainder of the project can be implemented (usually in the first sprint) that lay the foundation on which the remainder of the project can be built. Typical Infrastructure&Architecture user stories will revolve around the initial deployment and configuration of software products.

 
###Story Point Analysis

 

Once the initial backlog of user stories and tasks has been agreed upon, a story point analysis (also known as "planning poker") can be executed. The goal of planning poker is to estimate the relative level of effort required to implement each user story. Although the story point estimates are abstract, they feed into several important areas:

- The story point analysis can be used as the basis for a Level of Effort (LOE) analysis and project pricing
- The story point analysis highlights to the customer the effort required to implement the user stories
- The analysis can be used to estimate the resources required for the project
- If Agile project delivery is going to be used, the story point analysis can be used to plan the initial sprints

User stories are selected at random and all stakeholders asked to vote on how many story points, indicating the difficulty, or effort required to implement that user story. Typical methods of voting include holding up cards with the number of points, or using a smartphone app such as the ones her: http://agilescout.com/top-5-iphone-and-android-planning-poker-apps-agile/

When voting it is important that all stakeholders vote simultaneously to avoid bias.

The usual story point scale is as follows:

Points | Interpretation  
---|---|---
0 | Already implemented or trivial to implement 
1/2 |A tiny item
1 2 or 3 | A small item 
5,8 or 13 | A medium-sized item, For many teams, an item of size 13 would be the largest they would schedule into a sprint and larger items would be broken down into a set of smaller items. 
20, 40 | Large sized item, typically feature or theme-level stories. 
100 | A very large feature or an epic. 
00 | used to indicate that the item is so large it doesnt make sense to put a number to it
? | Used to indicate that the stakeholder does not understand the item and needs clarification

Following the vote, if all stakeholders have selected the same number, then consensus has been reached and these story points are assigned to the item. If the estimates are not the same, the team members should engage in a focused discussion to expose assumptions and misunderstandings. Typically, this discussion will focus on the high and low outliers. After the discussion, a revote is taken.

##Next Steps
The following actions can be performed after the Agile Specification session:

1. Write up of user stories, task breakdown and story point estimates for use by consultants who deliver the project
2. Level of Effort Analysis
3. Pricing Analysis
4. Formal Proposal and Quote
5. Preparation of Statement of Work

These steps will be detailed in other ACTIVITIES and TECHNIQUES.





