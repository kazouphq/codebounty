# Get paid to commit to an open source project

*DRAFT*

It sounds to good to be true ? Actually it is possible.
We at [Kazoup](http://www.kazoup.com) decided to pay you to develop and we will give it back to community.

## Why ?

We wrote monolith application in Python we went trough pain of writing authentication, Active Directory/LDAP integration, SMTP for sending emails etc.
It feels like reinventing the wheel every time you write application you need to write it all over again and again.
Yes we used open source libraries from great community at Github but these are just libraries still need work to be integrated with your application and you can't just run them.
What we need is the services library something which can be easily reused so we don't have to ever write LDAP/AD authentication ever again !!!!
This is really hard when your application is monolith and all code is tangled with your business logic.

Thats where microservices come in !!!

We decided its time to split our application into microservices since I was for some time interested in Golang we decided to switch language as well !

I looked through available libraries for writing microservices distributed system in Go and stumbled on beautiful [go-micro](https://github.com/micro/go-micro) by Asim Aslam ( yes I've seen go-kit)
It was extremely easy to start with and I really like  the abstraction and software engineering.
Lets just say it 'clicked' !

Go-micro comes with platform - set of services which are useful and necessary to run application but soon we notice we will need same services which are not there yet i.e. AD integration, SMTP service etc ..

We decided to outsource it as it should be fairly easy to implement them as there are no dependency on the rest of the system they are stand alone
small services responsible only for its own functionality - microservices !

Then it hit me why we don't offer bounty for writing this services and  give it back to the community.
Those services are not the core of our business they just building blocks which can be reused by anyone running [go-micro](https://github.com/micro/go-micro).
By open sourcing it we hope they can be improved with time and developers can get paid for contributing to open source project!

## How it works

We created list of microservices we need and we think can be reused in any application:

- [db-srv](https://github.com/micro/db-srv) - ElasticSearch driver for your existing db-srv £400
- [ldap-srv](https://github.com/kazoup/ldap-srv) - store configuration and authenticate against Active Directory £600
- smtp-srv - store SMTP config and send email £400
- flag-srv - features flags service £300

We have setup repositories for each of those with simple CI/CD pipeline CircleCi, DockerHub, coveralls.io and goreportcard.com
Each of the services has defined API interface and your job if you willing to take it is to implement functionality as per specification.
Feel free to fork and create pull requests once the pull request is accepted we will pay for winning code:

Code scoring:
- Does it run ? ;)
- Test Coverage
- Go Score Card
- Quality

## Getting pay

Once we accept the winning code we will need you to invoice us you can reach us at jobs@kazoup.com.

> Happy Coding !

Radek Dymacz CTO and Co-founder [Kazoup](http://www.kazoup.com)
