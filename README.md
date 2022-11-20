# GSoC-2022-Schemaorg-project-report

![Blogpost_869x400-GSoC2022-ShazmaSiddiqui](https://user-images.githubusercontent.com/43249198/202900638-503d45fe-3f92-43d5-854f-302c283debf6.png)

## Introduction
This repository contains details about my project schema.org in Google Summer of Code 2022 with Joomla!

**Project Idea:** [Schema.org Project Link](https://docs.joomla.org/GSoC_2022_Project_Ideas#Project_V:_Schema.org)  
**Project plan:** [Phase 2](https://docs.google.com/document/d/1gkzeRM99KB4mSkCpfc1A-PGgIB7vIKf43CdvI2yGUts/edit)  
**Project Repository:** [Project Repo](https://github.com/joomla-projects/gsoc22_schema.org/tree/dev)  
**Weekly Report:** [Report link](https://volunteers.joomla.org/teams/gsoc-2022-schema-org#reports)  
**Blog:** [Blog](https://community.joomla.org/gsoc-2022/gsoc-project-shazma-siddiqui-schema-org.html)  
**Joomla CMS Repository:** [Joomla CMS Repo](https://github.com/joomla/joomla-cms) 

## Major points covered

- System plugin working in a generic way
- Recipe implementation done with all field types from "Recipe" and "HowTo" + subform for "generic" title/value
- Schema.org is saved in the database and also prepared and save
- Merging/Display modules
- Book, Person, Organization, Event, Recipe, Blogposting
- Output in the frontend

## System Plugin 
[Link to PR](https://github.com/joomla-projects/gsoc22_schema.org/pull/2)

Adds schema form in all the allowed components (Content and Contacts for now)  

![Screenshot 2022-11-20 at 19-56-19 Articles New - Demo Website - Administration](https://user-images.githubusercontent.com/43249198/202907884-bf32809a-e94d-42eb-b6e7-d901680cc444.png)

## Schemaorg Plugins

[PR: Base Implementation](https://github.com/joomla-projects/gsoc22_schema.org/pull/6)  
[PR: Event Plugin](https://github.com/joomla-projects/gsoc22_schema.org/pull/8)  
[PR: Book Plugin](https://github.com/joomla-projects/gsoc22_schema.org/pull/9)  
[PR: Organization Plugin](https://github.com/joomla-projects/gsoc22_schema.org/pull/13)  
[PR: Person PLugin](https://github.com/joomla-projects/gsoc22_schema.org/pull/10)  

![Screenshot 2022-11-20 at 20-00-28 Plugins - Demo Website - Administration](https://user-images.githubusercontent.com/43249198/202907987-bf7ae045-8516-48fb-9b8f-e2f5f0fe6fdc.png)

## Service Interface

[PR: Service Interface](https://github.com/joomla-projects/gsoc22_schema.org/pull/11)

This provides each plugin an options to select allowed and forbidden contexts. Plugins won't be shown as an option to select as schema type in forbidden contexts. If there already exists a schema in forbidden context then it won't be deleted but unpublished which means that it will no longer be shown in the frontend.

![Screenshot 2022-11-20 at 20-02-40 Plugins Schema org Recipe Plugin - Demo Website - Administration](https://user-images.githubusercontent.com/43249198/202908115-31e6917b-2897-4b32-9dee-fa87bdef34d2.png)

## Recipe Plugin

**Major functionalites:**  

- All the empty fields are ignored
- Subform is converted into nested JSON
- Repeatable fields are turned into an array structure
- Image url is cleaned up
- Duration is normalized into ISO Duration format

![Screenshot 2022-11-20 at 20-16-45 Articles Edit - Demo Website - Administration](https://user-images.githubusercontent.com/43249198/202908944-710bc961-cbd8-4c79-80a7-430a64d6bd09.png)

## Generated Schema

![Screenshot 2022-11-20 at 20-21-37 Articles Edit - Demo Website - Administration](https://user-images.githubusercontent.com/43249198/202909101-647eb034-00bc-4da8-b42e-9e9b3f481cb7.png)

## Testing generated schema on Google Rich Results Test

![Screenshot 2022-11-20 at 20-25-48 Rich Results Test - Google Search Console](https://user-images.githubusercontent.com/43249198/202909204-1fa735ea-ac8a-432c-9208-2720a99b16a4.png)

## Output being pushed to the head tag of html in the frontend

![output](https://user-images.githubusercontent.com/43249198/202909495-e80be727-3a20-4c8d-8a18-be6aa129bc28.png)

## Generic field

Using this field a generic attribute in title=>value format can be added to the schema.

![Screenshot 2022-11-20 at 20-52-59 Articles Edit - Demo Website - Administration](https://user-images.githubusercontent.com/43249198/202910543-2824e38f-ad8e-4836-a03a-44bebadf0547.png)

**Updated Schema**

![Screenshot 2022-11-20 at 20-54-00 Articles Edit - Demo Website - Administration](https://user-images.githubusercontent.com/43249198/202910630-d2fd2b55-a84d-440d-8614-96d9aa928fd1.png)

## Mentors

A big thanks to my mentors [Benjamin Trenkle](https://github.com/bembelimen), [Tushar Malik](https://github.com/ditsuke), [Rishabh Ranjan Jha](https://github.com/rjharishabh) and [Anurag Kumar](https://github.com/anuragteapot). Thank You for being such amazing mentors, I can't imagine reaching the end of project without your support and supervision.

