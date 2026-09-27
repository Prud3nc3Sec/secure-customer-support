# Secure Customer Support & Fraud Incident Triage System

## Project Overview

A cybersecurity-focused customer support prototype for the banking and financial services sector.

The system demonstrates how customer support requests can be assessed for potential fraud indicators and either resolved normally or escalated for security investigation.

## Technology

- IBM Technology Zone
- Red Hat OpenShift
- IBM Verify – Authentication and access control
- IBM Guardium – Data protection and monitoring
- IBM QRadar – Security event monitoring and investigation
- NGINX
- HTML / CSS / JavaScript

## Workflow

Customer  
↓  
Customer Support Request  
↓  
IBM Verify  
↓  
Customer + Transaction Data  
↓  
Guardium  
↓  
Suspicious Activity Detection  
↓  
QRadar  
↓  
Fraud Triage  
↓  
Risk Assessment  
↓  
Resolve or Escalate

## Features

- Customer support request submission
- Banking-specific request categories
- Transaction review
- Fraud indicator detection
- High-risk and normal-risk classification
- Fraud case escalation
- Security event monitoring
- Synthetic banking data

## Deployment

The application was deployed as a containerized application on an OpenShift cluster provisioned through IBM Technology Zone.

### OpenShift Resources

- Project: `secure-customer-support`
- Deployment: `customer-support-app`
- Service: `customer-support-service`
- Route: `customer-support-route`
- ConfigMap: `customer-support-ui`

## Demonstration

The prototype demonstrates two scenarios:

### High Risk

An unauthorized KSh 85,000 transaction combined with failed login attempts and customer denial is classified as **HIGH RISK** and escalated.

### Normal

A KSh 2,500 account inquiry with no fraud indicators is classified as **NORMAL RISK** and proceeds through the normal support workflow.

## Data and Security

The prototype uses synthetic banking data only.

IBM Verify, Guardium and QRadar are mapped to their intended security functions. Direct live integrations were not represented where the required services were not exposed as application endpoints in the available TechZone environment.

## Future Improvements

- Live banking-system integration
- Real-time transaction monitoring
- Advanced fraud detection
- Role-based access control
- Automated security alerts
- Live IBM Verify, Guardium and QRadar integration
