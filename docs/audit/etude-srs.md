# Etude of Skill's Project SRS

## Objectives

The project aims to create a web application that allows you to manage your skills on your team.

## Lexicon

- **Skill**: a skill is a knowledge of a person.
  - *Example*: Git, Java, Angular, ...
- **Team**: a team is a group of people.
  - *Example*: The team of the project, the team of the company, ...
- **Person**: a person who has skills. Their can be a developer, a manager, a tester, ...
- **Prerequisite**: a prerequisite is rule that must be respected to have a skill level
  - *Example*: To have the skill level 5 on "Spring", you must have the skill level 6 on "Java".
- **Skill level [SL]**: a skill level is a level of a skill. It can be from 0 to 10. Each level represents a level of knowledge and mastery of the skill.
  - *Example*: The skill level 5 on "Spring" means that the person knows basics of Spring.
- **Skill validation [SV]**: a skill validation is a validation of a skill level. It's depends on prerequisites.

## Functional requirements
* CRUDs
  * CRUD od teams members [2.1.1](../SRS.md#__211-ability-to-add-edit-and-delete-team-members__)
  * CRUD of skills [2.2.1](../SRS.md#__221-ability-to-add-edit-and-delete-skills__)
  * CRUD of skill levels [2.3.1](../SRS.md#__231-ability-to-add-edit-and-delete-skill-levels__)
  * CRUD of prerequisites [2.4.1](../SRS.md#__241-ability-to-add-edit-and-delete-prerequisites__)
* Views
  * View of team members [2.1.2](../SRS.md#__212-view-of-team-members__)
  * View of skills [2.2.2](../SRS.md#__222-view-of-skills__)
  * View of skill levels [2.3.2](../SRS.md#__232-view-of-skill-levels__)
  * View of prerequisites [2.4.2](../SRS.md#__242-view-of-prerequisites__)
  * View of skill validation [2.5.1](../SRS.md#__251-view-of-skill-validation__)


## Questions
* [2.4.2](../SRS.md#__242-view-of-prerequisites__) : 
  * How to display the prerequisites ? A tree ? A list ? A table ?
  * `Ability to download the data: Users can download the prerequisites data.`: What is the format of the data ? CSV ? JSON ? XML ?
* [2.5.2](../SRS.md#__252-ability-to-view-validation-history__) 
    * `Ability to download the data: Users can download the validation history data.`: What is the format of the data?

## Data model

* Person
  * firstname (String)
  * lastname (String)
  * email (String)
  * skilllevels ? (List of SkillLevel)

* Manager extends Person


* Team
  * name (String)
  * members (List of Person)

* Skill
  * name (String)
  * description (String)
  * prerequisites (List of Prerequisite)

* SkillLevel
  * skill (Skill)
  * level (Integer between 0 and 10)

* Prerequisite
  * skill (Skill)
  * level (Integer between 0 and 1)


## Deployment

Frontend use Single Page Application (SPA) architecture. The backend is a REST API.
Deploy as Software as a Service (SaaS) on a cloud provider.
