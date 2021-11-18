# Open WIN Ambassadors
## Agenda and collaborative notes (wk3)

-----

**Important information**

- Date/time: Wednesday 17th November 2021, 09:30-11:00 (GMT/UTC)
- Join the call: MS Teams
- These notes: [https://hackmd.io/@FE_yEojCQPW4PD8RcTWR0A/HJyXDVGOF](https://hackmd.io/@FE_yEojCQPW4PD8RcTWR0A/HJyXDVGOF)
- Discussion: Please join the [Open WIN Slack](https://join.slack.com/t/openwin/signup) Channel #ambassadors-2021 or email cassandra.gouldvanpraag@psych.ox.ac.uk 


<mark>Yellow = action</mark>


-----

## Agenda
0. Participation guidelines and check-in
1. Aims of the session
2. Open data repository
3. Open Tasks repository
4. Open acquisition repository
5. Analysis wrapper
6. Background to Open WIN
7. Feedback

## Participants
(name / Pronouns / Department / git handles (GitLab;GitHub) / ORCID ID)
1. Cassandra Gould van Praag / she/her / Psychiatry / @cassag;@cassgvp / 0000-0002-8584-4637
3. Yingshi Feng / she/her / NDCN / [@yingshif](https://github.com/yingshif) / [0000-0001-9065-4945](https://orcid.org/0000-0001-9065-4945)
4. Bernd Taschler / he/him / NDCN-FMRIB / [@btaschler](https://github.com/btaschler) / 0000-0001-6574-4789
5. Verena Sarrazin/ she/her / Psychiatry / [@verenasarrazin](https://github.com/verenasarrazin) / 0000-0002-5796-5378
6. Dave Flitney
7. Matthew Webster
8. Paul McCarthy
9. Matt South
10. Duncan Smith
 
## Participation guidelines
- We value the participation of every member of our community and want to ensure that each of us has an enjoyable and fulfilling experience. Please show respect and courtesy to other community members at all times.
- We are dedicated to a harassment-free experience for everyone, regardless of gender, gender identity and expression, sexual orientation, disability, neurodiversity, physical appearance, body size, race, age, religion, politics or technology choices. We do not tolerate harassment by and/or of members of our community in any form.
- We welcome, support and respect eachother as whole people.
- We fall under the formal policy and reporting guidelines of the University of Oxford Bullying and Harassment Policy and we expect everyone to be a responsible bystander.

## Check in
How are you doing right now, in this moment?

-----

## 1. Aims
- Take a look at each of the Open WIN tools and think about what you could contribute to documentation and increase the uptake among WIN members. 
- For each tool we could think about: 
    - What has been achieved?
    - What is needed next?
    - Where is the documentation hosted?
    - What are the use cases?
    - How are people incentivised to use this?

## 2. Open Acquisition Repository
[https://open.win.ox.ac.uk/protocols/](https://open.win.ox.ac.uk/protocols/) (requires FMRIB VPN)
- Whats happening now:
     - List of issues: [https://git.fmrib.ox.ac.uk/acquisition/win-protocols-db/-/issues](https://git.fmrib.ox.ac.uk/acquisition/win-protocols-db/-/issues)
    - Improving the search tool
    - Download tracking, so people can see how often their protocol is used/visited
    - Documentation and use cases need to be written


## 4. Analysis wrapper
[https://git.fmrib.ox.ac.uk/fsl/wire](https://git.fmrib.ox.ac.uk/fsl/wire) (Public)
- Question for the project: How do you make analysis reproducible?
- Points to a dataset (currently OpenNeuro, but will be our data repo ultimately)
- Identifies a version of FSL to run with (singularity)
- **Assumes that the analysis script can be run by only identifying a directory/single script.**
- This wrapper is what you will share.
- Analyagous packaging for MEG (Andrew Quinn)
- What is necessary to get users?
    - People who are interested in making their analysis available
    - Finalise data repoistory
    - Where we stick the wrapper scripts (doi)
    - Modular conda FSL will be available internally in the next few weeks (externally next year perhaps_. Could make smaller, compartmentalised distributions to go with their scripts, but users would have to know which they need.
    - The majority of the work will be for end users to create their reproducible scripts.
    - **Templates, examples, documentation and recomendations for how to write reproducible analysis.**




## 3. Open Data Repository
[https://xnat.win.ox.ac.uk](https://xnat.win.ox.ac.uk) (requires University or FMRIB VPN)

- A web interface for allowing people to share their imaging (MRI and MEG) datasets
- Log in with WIN IT account
- Owner, member and collaborator levels of access. Owner has full privilages, member can upload/download, collaborator can only see.
- Currently hooked up to scanners in OHBA and MEG - new data acquired will automatically populate the repo. 
- Nice strength that you can look into directories before committing to download
- What do we need to get users?
    - Integration with other scanners in WIN (inc Brucker)
    - Integration a bit more throughly with calpendo
    - Prospective data adding should require very little action from the user. Retrospective upload requires a little more conversation.
    - User guide and use cases
    - Don't yet know what the public facing "front end"
- **Sharing data within WIN should be relatively straight forward in terms of ethics.** You will still need to be given access 


- **We haven't thought much about other data types, e.g. behavioural. How do we advise people to share these?**
- Tools are all WIN only. Openly developed, so others could replicate 




## 5. Open Tasks Repository
[https://git.fmrib.ox.ac.uk/open-science/tasks](https://git.fmrib.ox.ac.uk/open-science/tasks) (Public)



## 6. Background to Open WIN
- Clare Mackay will give a short presentation outlining the background to the Open WIN Project
- Slides from WIN launch (2017). What we were thinking when we put in the WIN bid and we decided one of our themes would be open imaging. 
- A lot of people came to open science throug hthe reproducibilty crisis. The answer to a lot of the problems is being more open/transparent in how we work.
- Also big translational value - why do we never get from clinical research to clinical practice? 
    - Need standards, validation
- It was easy to convince WIN that this is something we should do 
    - FSL has always been open and free to academic community). 
    - A lot of our platforms are open by descign (e.g. HCP, Biobank). 
    - As a community we have always been very open with eachothr (e.g. we can go into eachothers scratch on jalapeno, and it hasn't been a problem.)
- Now formalising and going into next era.
- We started with the technical challenges, but the ethical, governance, skills challenges are increasling recognised as significant
- All 15 WIN PIs agreed to share our outputs and "document how we got there", so we can share our learning. 
- Vision Statement: WIN will become and open science community with a positive culture for sharing data, tasks and tools, to improve transparency, reproducibiliey and impact...
- Sharing Scenarios
    - Output based: As you develope your paper, you put your outputs into a structure for others to access
    - Project based: data can be selevtively accessed to fit a requirement of a new project (e.g. participant characteristic).
- Share across different levels. Set up the infrastructure to enable you to share publically when you are ready to do so. 
- What do we ned to do to support people to share their pre-processed data? We haven't got any convensions or recomendations for how this should happen. 

What has changed since 2017?
- Cass hiring represented a shift in the emphasis into the "deeper levels of the iceberg". 

How does it interact with the University?
- WIN sits across at least 3 Departments. The department is the unit of control, as the university sees it. 
- We intend to take our learning to the wider neuroscience community
- Similar initiative in the university (e.g. BNDU)
- University signs things like "concordat for researcher development", but of the interactions that peoplle have are at the level of the facility and the department. 

Have we thought about incentives?
- Laurence's talk on why we should be open scientists - good for you.
- Alzheimers UK talking about chaging their forms to make all research outputs count in applications. 
- Incentives are coming to us. 
- University level: re-grading/promotion templates don't current include specific reference to open science (DORA). Should we all have a CV section "contributiosn to open science"
- These things really do count within the university, even if they are not written on paper. 

What we our ambassadors motivations into open science?
- The mission statement is internally focused, but is there space to talk about influenceing the wider communmity? Yes :)
- 


## 7. Feedback on this session
<mark>Please add a few words to each of the sections below so we can improve the expereince of others.</mark>
### What worked well?
-
### What surprised you?
-
### What would you change?
- 
### What would you like to know more about?

