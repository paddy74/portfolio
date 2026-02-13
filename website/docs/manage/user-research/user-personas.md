# Defining User Personas

User personas help describe the users of a product or service.

## Lightweight User Personas

Lightweight personas do not emerge from user research but instead are driven by the experience and assumptions of the product team and key stakeholders. Lightweight user personas provide value by aligning the team's different assumptions into explicit commonly understood definitions.

- [Example Lightweight User Personas](./ex-light-personas.md)

## Qualitative User Personas

Qualitative personas are driven by solid exploratory qualitative research, such as interviewing users, with a small-to-medium (5-30) sample size, and then segmenting users based on shared attitudes, goals, pain points, and expectations.

A qualitative persona may include the persona's age, education level, years at the organization, motivations, traits, current actions, pain points, key quotes, and opportunities.

- [Example Qualitative User Personas](./ex-qualitative-personas.md)

## Role-Based (Functional) Personas

Role-based persona are driven by a user's individual job functions and role within an organization.

### Example Role-Based Personas

1. **Admin**. The persona who is the highest point of escalation across every environment. This should be a highly restricted role.
2. **Data Engineer**. These individuals build data pipelines and should have access to their own assets and environment. These personas should also have visibility of commonly shared assets that do not contain sensitive information but whose metadata and configuration data are useful for reference.
3. **Data Scientist/ML Engineer**. These individuals develop models and experiments and should have access to their own assets and environment.
4. **Data Analyst**. Personas focused on querying various data sets whose scope on objects should be limited. Complexity of setting them up comes from access to data itself, and the permissions they are granted on specific data assets, but data object privileges are out of scope for this work.
5. **DevOps Engineer**. This persona is focused on DevOps and SDLC and will help review code and move projects into production. We believe they should have access to most UAT/PROD assets to achieve these goals. However, for PROD specifically, we recommend this persona to be restricted to Service Account/Service Principal users rather than human users.
6. **Application Support**. These play a crucial role in helping data engineers, data scientists, analysts or even deployers debug their application across the different environments and should have the right level of access from the start to be able to assist.
