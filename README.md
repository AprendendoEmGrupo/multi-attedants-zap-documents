## About project 

Create a system where a person can have more than 1 attendant answering questions using a single What'sapp.

The project will be a project site where the focus is to gain experience, knowledge and help people gain experience to get a job or an opportunity where it pays better.

## Requirements

- Show incoming text messages sent via Whatsapp on the dashboard.
- Allow attendant to initiate a call.
- Allow attendant to send text message to reply.
- Show audio messages, image or documents received via Whatsapp on dashboard.
- Enable attendant to send image, audio and documents to reply.
- Allow attendant to finish a service. NOTE: Attendant can start more than one service at a time.
- End the service automatically after 30 minutes without interaction.
- Start whatsapp session.
- End whatsapp session. 
- After finishing the service send a request for evaluation of the service.
- Dashboard that shows the following information: care finished in a period, open care in a period and total care finished per attendant in the period, total open care per attendant in the period.
- List service
- View details of the service where it lists the messages received and sent by the attendant

## Non functional requirements

- The admin can create new users. It is either Admin or Attendant user. NOTE: Admin user can create new Admin and Attendant users, but can't delete any user.
- Admin user will have full access to the system
- Attendant will have access only to the chat part of the system
- Login to access the application
- Reset password

## Technologies

- Database
  - Postgresql
- Backend(api)
  - Firebase(firestore) like websocket server.
  - Firebase cloud storage to upload files.
  - Node.js
  - Typescript
  - Nest.js
  - Jest(Unit test)
  - Prettier
  - BullMq + Redis(Queue)
- Backend(Bot)
  - Firebase cloud storage to upload files.
  - Node.js
  - Typescript
  - Jest(Unit test)
  - Prettier
  - BullMq + Redis(Queue)
- Frontend
  - Tailwind
  - Typescript
  - React.js
  - Vite.js
  - Websocket(firebase sdk-js)
  - Jest(Unit test)
  - Prettier
- Mobile
  - Typescript
  - React native. OBS: verificar se existe lib para gravar áudio.
  - Styled component
  - Websocket(firebase sdk react native)
  - Jest(Unit test)
  - Prettier
- Infra
  - Vercel(Frontend)
  - Pm2
  - EC2
  - Load balancer. Warn: no need first moment
  - Auto autoscaling. Warn: No need first moment.
  - RDS. Warn: digitalocean has solution to database more cheap.
- Devops
  - Github actions para automatizar CI / CD
  - Docker and Docker compose. Warn: dev environment to api
Others
 - Git
 - Github
 - Doppler e infisical(secret manager)
 - Sentry(track errors in api and cronjob) 

## How to work Github project management task

- Backlog: in this column you all thing client(owner of project) request
- Todo: in this column you have all tasks necessaries to complete the backlog task.
- In progress: in this column you have all tasks the dev team your current.
- Validate PR's: in this column you have all tasks the dev team completed and open pull request to validate
- Done: in this column you have all tasks validated and completed. In this step all tasks are branch master.

### Rules

- Each developer can have one tasks in column **In progress**
- After completed task and open pull request you need to move task for column **Validate PR's**

## How to work with git in project

- Branch **master** code go to production
- Branch **staging** code go to staging. Warn: in future can have staging environment to validate if feature is ok before send production.
- Branch **Develop** all new feature created based this branch.

### Rules 

- To write commit message in english
- Never send your directly to branchs: **master**, **staging** and **develop**
- Always you complete your feature open pull request to branch **develop**
- When create branch for new feature you need use this pattern: feature/shor_description_about_task

### Example how to work: feature login

- Execute command: **git checkout develop**
- Execute command: **git pull origin develop**
- Execute command: **git checkout -b feature/login**
- Execute command when complete task or want send code to Github: **git push origin feature/login**
- Access Github 
- Open pull request to branch **develop**

## How to report error, some problem as your task or difficulty your task

- Send what's task you working
- Send error
- Send what your tried to resolve

## For example:

Hi, my friend! I working login feature, but i tried install jsonwebtoken module and receive this error: **the module jsonwebtoken not found**. I search about solution in google but any solution work. I tried this links: https://www.youtube.com/ and https://www.youtube.com/

## The documents:

- [Database diagram](./database-diagram.png)
- [Architecture diagram](./architecture.png)
- [Explanation about architecture diagram](./Architecture.md)
- [Flows of application](./flow-pipeline.png)
- [Pipeline diagram](./flow-pipeline.png)
- [Explanation about pipeline](./Pipeline-ci-cd.md)


## Links helpful

| About    | Language | Links |
| -------- | ------- | ------- |
| Queue  | Portuguese  |  [Click here](https://www.youtube.com/watch?v=U5h6B7eSiAE)    |
| Websocket | Portuguese     |    [Click here](https://www.youtube.com/watch?v=RwUbUnPdWqs)      |
| Redis    | Portuguese | [Click here](https://www.youtube.com/watch?v=HMEwYxXFTjM) and [Click here](https://www.youtube.com/watch?v=1Tfzm7Wfk74)         |
| BullMq + Redis        |  Portuguese        |   [Click here](https://www.youtube.com/watch?v=uonKHztGhko)      |
| Firebase storage | English | [Click here](https://www.youtube.com/watch?v=-IFRVMEhZDc) |
| Firebase firestore | Portuguese | [Click here](https://cloud.google.com/firestore/docs/create-database-web-mobile-client-library?hl=pt-br)



