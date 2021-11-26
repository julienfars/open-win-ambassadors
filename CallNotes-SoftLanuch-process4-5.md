# Open WIN Community feedback on data sharing processes 4-5

-----

**Important information**

**Where**: Teams

**When**: TBC

**Contact**: Email Cass:
[cassandra.gouldcanpraag@psych.ox.ac.uk](mailto:cassandra.gouldcanpraag@psych.ox.ac.uk)
or message on Open WIN Slack #data-sharing-decision-tree

**Material we will be reviewing**:
- [Decision tree](https://git.fmrib.ox.ac.uk/open-science/community/data-sharing-decision-tree/-/blob/master/docs/decision-tree.md)
- [Appendices](https://git.fmrib.ox.ac.uk/open-science/community/data-sharing-decision-tree/-/blob/master/docs/decision-tree-appendicies.md)

-----

## Agenda



1. Introductions
2. Participation guidelines
3. Using this document
   1. Add your name if you'd like to be listed as a contributor
   2. "+1" where you agree
   3. All write everywhere! Individual comments can be anonymous.
4. Feedback on each step
5. Feedback on the day

## Participants

(Name / Pronouns / Department / GitLab user ID - or "none" / ORCID ID (for attribution)
1. Cassandra Gould van Praag / she/her / Psychiatry / [@cassag](https://git.fmrib.ox.ac.uk/cassag)
2. Ludovica Griffanti / she/her / Psychiatry / [@ludovica](https://git.fmrib.ox.ac.uk/ludovica) / 0000-0002-0540-9353
3. Jessica Walsh / she/her / NDCN/WIN / [@ndcn1073](https://git.fmrib.ox.ac.uk/ndcn1073)
4. Christoph Arthofer/ he/his / WIN/FMRIB / [@cart](https://git.fmrib.ox.ac.uk/cart) / 0000-0003-1474-9963
5. Mats van Es/ he/his/ WIN-OHBA / [@psych1435](https://git.fmrib.ox.ac.uk/psyc1435)
6. Marieke Martens / she/her / Psychiatry / [@mmartens](https://git.fmrib.ox.ac.uk/mmartens) / https://orcid.org/0000-0003-0108-1327
7. 

## Participation Guidelines
- We value the participation of every member of our community and want to ensure that every contributor has an enjoyable and fulfilling experience. Please show respect and courtesy to other community members at all times.
- We are dedicated to a harassment-free experience for everyone, regardless of gender, gender identity and expression, sexual orientation, disability, physical appearance, body size, race, age, religion, politics or technology choices. We do not tolerate harassment by and/or of members of our community in any form.
- We fall under the formal policy and reporting guidelines of the [University Bullying and Harassment Policy](https://edu.admin.ox.ac.uk/harassment-policy) and we expect everyone to be a [responsible bystander](https://edu.web.ox.ac.uk/bystander)

## How do you feel about data sharing? How does your PI feel about data sharing?

**Imagine you are a WIN researcher asking "*Can I share my data?*", or "*How can I share my data?*"**

- 

The "decision tree" document and appendices should guide you through the necessary stages to prepare your data for sharing.

**This is not a trivial process, but the purpose of this guide is to help you, not scare you!**

Today we are not writing a "user guide", simply determining whether the plans we have developed will work for you, if we have missed anything, or if there is anything we need to do to support you further.

**You are the ones who will be sharing and receiving credit for your data, so we want to make it easy for you!**

## Feedback on each step

While we're working through each step:
- Do you know how to do this thing?
- Does this flow work for your data?

## DPIA
- Jess: CTRG are happy that if your study is sponsored by them then you don't need to do a DPIA (Jess will forward and email)


### Process 3: De-identification
Personal data can not be made fully anonymous, only "de-identified" to the best of our practical ability. This process describes appropriate de-identification steps to take.

Add below any comments about each of the steps in this process.


#### Unique dicom fields
[See appedix 1](https://git.fmrib.ox.ac.uk/open-science/community/data-sharing-decision-tree/-/blob/master/docs/decision-tree-appendicies.md#dicom-scrub)
- Do you routinely or infrequently rely on any of these fields? Which would be problematic to remove? Any that should be kept for everyone?
- How would you like scrubbing to be applied? A default set of fields removed with optional extras (opt in), or all fields by default with option to keep some (opt out). At what stage of the process? Before upload to XNAT or after?
- How much date information would you like to keep (for example to handle a "product recall" scenario if a scanner fault was detected)?
- Patient size and weight are in there for the safety of the MR system. Did you know they were in there? Do we need to educate about what is sensitive in headers?
- Risk that not all scanner manufacturers have the same tags. An anonymisation tool may miss some tags.

##### Date of birth
- People wouldn't routinely go back to the dicom to get DOB (or year), unless you have acquired the data from someone else. Useful sanity check. +1
- When sharing data with inducstry recently, industry partner was happy to keep year of birth only
- Radiographers really lilke to keep full date of birth.
- Sharing dicoms or nifti? P1vital wanted the dicoms.
- **table position is used in biobank pipeline (coordinatre in the scanner)**. Used in an IDP. 

##### Patient sex
- You would expect this to be someonwhere else, but good for sanity check. +1
- Same with size and weight. +1


##### Time and date
- acquistion time can be used to control for arousal. I would not put this in a normal database of metadata, but it is something we might come back to with a secondary hypothesis. 

##### Which scanner
- Device serial number and insitutional address. Multi centre covid study use this information...! Biobank pipeline contrains a call to the pipeline to find out the address...! 

##### Study description
- One instance with a participant which was scanned over different projects and combineed to make a new one. 

#### Defacing and skull stripping
- The face is usually critical for coregistration. What would be the advice; sharing the defaced structural + the coregistration info (that was derived from the complete structural)? +100. Note this is a unique 
- usually get defaced images with the skull. 
- skull gives a bit of reference (SIENA)
- Non-skull stripped images are used to create a referfence space for creating them oxford template [Oxford-MM-1](https://git.fmrib.ox.ac.uk/cart/oxford-mm-templates); MMORF can be used to register non-skull stripped images to this template
- non-skull stripped images for olfactory bulb segmentation.


#### Quality control
- Mriqc can be run on XNAT. Would you run mriqc before your own analysis anyway?
- mriqc still being used
- usually done manually/visally.
- People would be happy to run a simple qc as a recomended step
- biobank by default extrqacts some qc measures (qc IDPs) but it doesn't exclude. 
- **Talk to Fidel about the biobank pipeline**


### Process 4: Metadata

Your shared research data should be supported by additional metadata to make it findable, accessible, interoperable, and reusable ([FAIR](https://www.go-fair.org/fair-principles/)). This process helps you identify what metadata will be necessary to make your data FAIR, how to collate it, and how to sufficiently describe it.

Add below any comments about each of the steps in this process.

#### electrophys
- **We don't know much about electrophys metadata...***
- Ususally you have MRI as well
- head circumference, height, weight
- which things are recorded as standard (e.g. dental wire is important to know)

#### data dictionary
- not unfamiliar with these, expect to have in place. You learn the hard way!!

#### Image metadata
- dcm2niix is maybe comparable with the BIDS .json.
- downloaded data from the magnet also comes with a .json
    - what is in the non-BIDS .json which comes with a normally downloaded form the magnet nii.
- don't forget about the acquisition database. Could recommend that you share the entire acquistion protocol. **think about de-identifying the acquisition reports**
    - make sure all the radiographers positioning etc info is included (the radiographers protocol). Is this generated by default? If yes, the radiographers should upload (if no privacy concerns)



#### Experimental protocol
- Usually share the experimental script (e.g. in psychtoolbox, psychopy), along with a brief description in a README file. 
- What about more detailed stuff about the session design. Some information might be on the trial registry. 
- Could share a SOP for the testing, if you have that, but not everyone would ahve that. 
- In the paper you would describe briefly
- More detail would be in the ethics. Could share the **study design section**. Don't need to share the whole docuemtn as this has other info (e.g. recriutment, resaearchers names). 
- protocols.io. really good for wetlab experiments (has fields for doses etc.)... Not sure if it is well suited to our standard studies
- Study design section
    - wouldn't have anything specific to the participant, but it would have the different tests, questionnaires etc. 
    - might also have things in there that you wouldn;t want to share. 
    - Exclusion criteria might also be useful, but not in this section.
- **How would we make sure useful things about blinding, counterbalancing etc is communicted**
Mats: In my experience , most often a file is shared (e.g. .mat file), containing some subject specific information, including counterbalancing, amounts of sessions completed etc.


### Process 5: Sharing and attribution

This process describes how to upload your data to XNAT and make it citable. You are also asked to consider whether the standard WIN XNAT Data Usage Agreement (DUA) is appropriate for your data.

Add below any comments about each of the steps in this process.

#### Upload to XNAT
- Who would you like to give internal access to your project? You, your PI and XNAT admin? Your jalapeno user group?

#### Data freeze
- some people might release in stages to give themselves a "headstart", for example some minimally preprocessed data.
- P1vital want data on a rolling basis (within 3 days of scanning)
- Maybe different versions of templates. New releases.


#### Generate a DOI
- Mats: For the Donders Repository, a DOI is created as you create the repo - this is a placeholder that can for example be written in your manuscript, but the data will only be published after review.

#### Data usage agreement
- Which statement do you prefer about authorship on papers which re-use your data:
  1. "The data generators shall not be included as an author of publications or presentations without consent."
  2. "Neither the Donders Institute or Radboud University, nor the researchers that provide this data should be included as an author of publications or presentations if this authorship would be based solely on the use of this data." +1
Mats: People that are accessing the data have to agree they won't try to de-anonymize the data

#### Approve public sharing on XNAT
- How would you like to stage the approval process? Would you like the PI to approve? Email warnings / invitations? Would you like to see a review summary of the de-identification processes completed (e.g. a checklist read from the image metadata)?
- How do you think the access of external users to be managed? Should they have to create accounts? How will accounts be verified (e.g. ORCID or institutional?)? Should accounts be closed after a fixed period?
- What metrics would you like to know about how your data is accessed?


#### Approval of access
- ORCID? Insitutional email?
- Log of who accesses the images
- password provided by us and renewed frequently (request from an ethics team for covid study ?OCMR)
- BHC requests (and DPUK) have to submit a request to access the data. The more things you ask for, the more you have to review (then need a review committee).


#### Citation and authorship
- this is another conversation...




-------

## Feedback on the meeting
- Please take a few minutes to tell us how this day went for you! Your feedback is invaluable to making this community and these events work.
- You are also welcome to email feedback to [cassandra.gouldvanpraag@psych.ox.ac.uk](mailto:cassandra.gouldvanpraag@psych.ox.ac.uk)


#### What worked?
- Having an open conversation
- Good sized group for open discussion
- Having different perspectives from different kind of researchers was very useful 
- Quick way of gathering information we all have in our head but which is not directly out there to find online for example 

#### What didn't work?
- comment here

#### What would you change?
- Some info on what we were going to talk about in the meeting would have been helpful to know beforehand. 

#### What surprised you?
- comment here

thank you for organising again Cass! :)

-------

## Post-meeting summary
-
