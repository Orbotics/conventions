# Conventions

This markdown file is meant to outline the conventions for workflow and processes for robot code. These rules are specific to Orbotics FRC Team 10152, but feel free to use or modify them for your own team as well!

## Table of Contents
- [Project Management](#project-management)
  - [Sprints & Season Adjustments](#sprints--season-adjustments)
  - [Task Creation & Assignment](#task-creation--assignment)
  - [Story Points & Estimation](#story-points--estimation)
  - [Ticket Status Workflow](#ticket-status-workflow)
- [Git Version Control](#git-version-control)
  - [Branching Strategy](#branching-strategy)
  - [Commit Message Guidelines](#commit-message-guidelines)
  - [PR Review and Approval Process](#pr-review-and-approval-process)

## Project Management

### Sprints & Season Adjustments
We aim to make the robot software development process similar to a traditional software engineering process. During the FRC build season (6-7 weeks) and throughout the offseason, we will be coding in "sprints". Used in professional environments, code sprints are short time-boxed periods (typically one to four weeks), where there are a defined list of tasks to be completed. For Team 10152, we will be adjusting the length of sprints based on the stage of season. For example, weekly sprints may be set during the build season due to time constraints, and monthly sprints during the offseason. 

<br>

### Task Creation & Assignment
To facilitate sprints, we will be using [`Taiga`](https://taiga.io/), a free open-source project management tool. Since the Software Captain acts as a project manager, the `Scrum` template is most optimal. After kickoff weekend discussion, the Software Captain should create tickets in advance (preferably for the next 2 weeks) and assign them to the appropriate Directors and Specialists (roles specific to Team 10152).  

<br>

<img width="3837" height="1765" alt="Screenshot 2025-08-22 122344" src="https://github.com/user-attachments/assets/1ce29333-4792-475a-82b8-1657f978e032" />

<br>

To add a new ticket, navigate to [Team Tree](https://tree.taiga.io/project/ryanzhangofficial-orbotics-frc-team-10152/) (by invite) and click on "Add New User Story". In industry, teams call new tasks "User Stories" because new features are added in the perspective of the end-user. However, as FRC Robotics students we will refer to tasks as "tickets".

<br>

<img width="3839" height="2048" alt="Screenshot 2025-08-22 123114" src="https://github.com/user-attachments/assets/4f840174-5ffd-4411-a57f-b371c00b05a7" />

<br>

### Story Points & Estimation
When you create a ticket, make sure to include a concise title, detailed description, and attachments if needed. Story points are a core part of the software project management. Because we are working on robot 
code, ignore the UX, Design, and Frontend rows, and only add to the Backend row. In the workplace, 1 Story Point is equivalent to a day or half a day's work. Team 10152 will regard one story point as a day's work.  

<br>

<img width="3838" height="2043" alt="Screenshot 2025-08-22 123339" src="https://github.com/user-attachments/assets/22b949a6-18a7-4afd-b6ab-6ce6e01811c2" />

<br>

As a software captain, please use your best judgement when assigning story points to tickets. However, it won't always be perfect, and that's ok. There will be huge overestimations and underestimations, but you will develop an intuition throughout the year. Most importantly, encourage communication with your team to make sure everyone can manage their workload. FRC is supposed to be a great learning experience, but lots of fun at the same time!

<br>

### Ticket Status Workflow
Taiga allows users to configure the status of tickets. If you're working on a ticket, please set status to `In Progress`. If you're ticket is ready for review, please switch to `Ready for Test`. Once the ticket's corresponding PR has been reviewed and approved, the Software Captain will merge the PR and set status to `Done`.

<br>

<img width="3839" height="2054" alt="Screenshot 2025-08-22 175712" src="https://github.com/user-attachments/assets/f2eaf96a-95ac-4f39-96b9-e52c1b578bcf" />

<br>

## Git Version Control
This markdown file is meant for outlining conventions. If you want to learn git, feel free to explore this [document](https://github.com/ryanzhangofficial/git-guide) or the official [Github documentation](https://docs.github.com/en).

### Branching Strategy
There will be two core branches: the `main` branch which consists of the final robot code for deployment during competitions, and the `dev` branch which will include all approved code. You may wonder, why do we distinguish between these two branches? This is mainly due to how [sprints](#sprints--season-adjustments) work. Approved code during a sprint will be merged into the `dev` branch, and all new code will be merged into the `main` branch at the end of the sprint. 

<br>

<img width="3837" height="2048" alt="Screenshot 2025-08-23 121131" src="https://github.com/user-attachments/assets/a94b267d-4299-4976-a478-b3326851b1ae" />

<br>

However, as a developer, most of your interactions with the robot code repository will not be with those two branches, unless you're responsible for git actions, and will be working on separate branches. Each ticket has a corresponding number and name. When creating a new branch for your ticket, please refer to the convention of `{your name}/{ticket-number}/{ticket-name}`.

<br>

<img width="2405" height="146" alt="Screenshot 2025-08-23 121812" src="https://github.com/user-attachments/assets/3b8db49f-09ff-417d-856a-cfa3a0e4a869" />

<br>

<img width="3839" height="2051" alt="Screenshot 2025-08-23 122043" src="https://github.com/user-attachments/assets/c920fc50-1834-4b56-884d-d4daa0f02850" />

<br>

### Commit Message Guidelines
Having an orderly set of commit guidelines is crucial to any git workflow. This ensures organization and makes it easier to go through logs as the codebase becomes larger. For Team 10152, the core commit types are:  

- **Feats** — use `Add`, `Update`, or `Remove` at the start of the message  
- **Chore** — routine maintenance tasks such as formatting or cleanup  
- **Fix** — resolving a bug in the current code  

The table below shows the expected formats for git commit messages:

<br>

| Type   | Format                 | Example Commit Message             |
|--------|------------------------|------------------------------------|
| Feat   | `Add <description>`    | `Add drivetrain subsystem`         |
| Feat   | `Update <description>` | `Update autonomous routine`        |
| Feat   | `Remove <description>` | `Remove unused sensor logic`       |
| Chore  | `chore: <description>`  | `chore: formatting`               |
| Fix    | `fix: <description>`    | `fix: motor controller ID`        |

<br>

### PR Review and Approval Process
