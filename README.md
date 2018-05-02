# Credit Card Application - jBPM Case Management


A case project with human tasks and different milestones. <br>It shows:
 - Case mgm features
 - Case file definition
 - Milestones
 - Case users and groups
 - Case conditions
 - Case role assignments vs Human tasks role assignments
 - Case data
 - Case dynamic human tasks
 - BPMN Human tasks
 - SLA

This sample project is used to follow the process of a new credit card request.
The request is made by a customer to his own bank.
The overall case project must b completed in 5 minutes (SLA); if the SLA is not met, a new User Task is assigned to the administrator
<br>(usage of org.jbpm.casemgmt.impl.wih.EscalateToAdminSLAViolationListener)


## Credit Card Application - Case overview

![alt text](https://github.com/hifly81/bpm-credit-card-application/blob/master/src/main/resources/com/redhat/creditcardapplication/com.redhat.creditCardApplication-svg.svg)

## Credit Card Application - Case assignments

Owner:
 - admin

Groups:
 - customer
 - bank_operator
 - bank_supervisor

## Credit Card Application - Case Milestones

#### Milestone 1 - Customer Form<br>
 Case activities:
- Customer Form User Task<br>
    actor: customer

#### Milestone 2 - Customer application check<br>
 Case activities:
 - Bank Balance Check User Task<br>
     actor: bank_operator
 - Customer debt position User Task<br>
     actor: bank_operator
 - Credit Card Final Approval User Task<br>
     actor: bank_supervisor

## Credit Card Application - SLA policy
 Case overall SLA due date: 5m (5 minutes)<br>
 Bank Balance Check User Task due date: 1m (2 minutes)<br>
 Customer debt position User Task due date: 2m (2 minutes)<br>

 if the SLA is not met, a new User Task is assigned to the administrator
 <br>(usage of org.jbpm.casemgmt.impl.wih.EscalateToAdminSLAViolationListener)
