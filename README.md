# CAP-demos
CAP demos

## Stateful app
`cd 07-shared-state/stateful-app`

`cf push --no-start`

`cf create-service redis 4-0-10 stateful-app-redis `

`cf bind-service stateful-app stateful-app-redis `

`cf restage stateful-app `

`cf start stateful-app `

Goto the created weblink 

Change the number of instances, either in stratos or by command: 

`cf scale stateful-app -i 8`  
