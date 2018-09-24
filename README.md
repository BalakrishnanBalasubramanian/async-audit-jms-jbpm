# async-audit-jms-jbpm

Refer the articles listed below for details on how to setup asynchronous audit logging in jBPM 7. Asynchronous logging helps in two ways:

1. Possibilities to improve the overall performance of the jBPM engine by offloading the audit logging to a message listener (_message is first pushed from jBPM to a JMS provider and a custom listener automatically picks up the messages and log them into audit data tables_). This when compared with the default setup (_where database logging of both engine data + audit data happens in a single XA transaction_) should be much faster. 

2. Provide opportunities to push the full audit data to external data stores like Elastic to support faster deep search and consolidation. 

```
a. https://access.redhat.com/solutions/3301681
b. https://access.redhat.com/solutions/2178521
```

