3 common pitfalls in microservice integration and how to avoid them

BERND RÜCKER

- circuit breaker
    - method to recognize one of the service is not acting correctly
    - fail fast is important, other services can't spent resources waiting on the burnt service
    - hystrix (deprecated for JAVA)
- stateful retry
    - handling state
        - persist
        - scheduling, versioning
    - state machined, workflow engine
        - AWS step founctions
        - netflix conductor
        - zeebe

- the conflict between what is successfull response
    - we return 202 as notification of receiving the request and doing our best to complete it
    - we can't immediatelly returns eg PDF

- idempotency

- asynchronicity
- message bus

- distributed transactions
    - combinate multiple transactions across distributed system
    - saga pattern
        - 
        
- what if 


LINKS
https://camunda.com/