# Guidance

This document offers guidance on the scope and usage of HTCDS.

## Scope of HTCDS

The scope of HTCDS is related to a subset of all of the components that typically make up a case management system (CMS). Whether it's a helpline system of victim case  service, a CMS is normally composed of a stack of services and components that enable different features for users. These are described below.

| CMS Services                | Description                                                  |
| --------------------------- | ------------------------------------------------------------ |
| User Interface and Channels | Case management systems can normally be accessed via desktop and mobile devices. These channels can be enabled by Platform-as-a-Service (PaaS) cloud services, bespoke platforms, or office-based products such as spreadsheets. Typically the design is customized to the needs of users, whose roles may vary. |
| Process and Security Model  | Process models include human-based workflows such as approvals and task management; and system-based workflows, such as data retention policies and disaster-recovery. Security models include authentication, authorization and audit mechanisms. Some configuration could be included in ”Platform Configuration” depending upon the platform selected. |
| **Data Model**              | **Data models are the schemas that define how records stored in a case management system. Typically, fields (columns) are associated with tables (objects / sheets) which are related. Fields have a type which describe the way in which data within a record is stored.** |
| Platform Configuration      | Most case management systems are built on an existing technology platform (or platforms) which are often enabled through a cloud service. The design would include the configuration necessary to manage the system or service as a whole. It could include aspects related to scalability, resilience, network security, user management, backup/recovery and general system administration. |

HTCDS is not intended to standardise all of these services and components because there are many types of implementations and services which are designed to support different contexts. Rather, HTCDS will centre on the **data model**.

In reality, there is often an overlap between a core data model that describes a trafficking case and other aspects that can imply a business *process*. For example, documenting a referral in a standard might imply a referral process. A case status field might imply a basic case lifecycle process. HTCDS is not intended to standardise all of the many important aspects of case management processes and methodologies. But where there is an overlap, HTCDS highlights this and offers the implementing organisation to apply it within their processes in a way that works for them.

## Data Model

Sophisticated case management systems contain hundreds of fields. Many could be contextualised to a process, region or a organisation’s methodology. But at a high level, the core data model of every system can be described within the context of a person, a case and the various contextual information that links the person with the case.

The scope of case data in systems and services can vary significantly. For example, helplines and victim rehabilitation have very different models. This table below is a simplified summary of a data model designed to express the context of the standards offered by HTCDS.

| Context                      | Description                                                  |
| ---------------------------- | ------------------------------------------------------------ |
| **Person Data**              | Person data may include identifiable data such as name, address, gender, occupation, family, etc. In general, the data may be separate but related to the Case record. The person is related to the case and may be a victim/survivor, perpetrator or other person connected to the organization’s Case work. |
| **Person Case Context Data** | Case context data represents how a person is connected to the case. This may include perpetrator or victim data about the nature of the trafficking or exploitation for a particular Case. Examples include methods of control, types of exploitation and relationships between people in the context of the Case. |
| **Case Work**                | ”Case” is typically used to articulate the work planned and performed by an organization to support one or more victims/survivors of human trafficking. In a helpline it tracks status over several months across various activities and phone calls. The data within “Case work” can include case status updates, activities, related organizations, impact/outcome measurements, referrals and personal case history. |

HTCDS is not intended to be a constraint and it would be normal for systems and services to expand upon the core model to meet other specific requirements. Indeed, it would be attractive to consider innovations developed by organisations around the core data model which could be incorporated into the standard in the future.
