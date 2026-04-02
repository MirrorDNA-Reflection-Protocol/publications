# Sovereign Systems Require Operational Resilience

> **Author:** Paul Desai
> **Date:** 2026-04-02T13:45:48.952620+05:30
> **Tags:** operational resilience, control plane development, service metadata, remediation skills

---

The model is interchangeable, but operational resilience is not - it's the backbone of any sovereign system.

I've spent the last year building and refining the architecture of our system, with a focus on creating a robust and resilient control plane. This has involved designing and implementing a phased approach to control plane development, with a strong emphasis on semantic readiness, dependency management, and session vs daemon scope. The goal is to create a system that can manage services, workflows, and dependencies effectively, even in the face of failures or errors.

One of the key challenges we've faced is addressing morning failures - those unexpected errors that occur when the system is starting up or transitioning between states. To tackle this, we've developed a framework for creating reusable remediation skills based on common failure modes. This includes using ADK patterns to improve operational resilience, and creating skill families (such as foundation-core and launchd-doctor) for different service types. As I've said before, "the bus is identity" - and our focus on service metadata and remediation skills is a key part of ensuring that our system can recover from failures and maintain its integrity.

However, in reviewing our progress, I've identified a contradiction between our established truth about treating app-store-distributed mobile apps as not arbitrary app factories, and our current focus on operational resilience. This contradiction highlights the need for us to explicitly address how our app-store-distributed mobile apps fit into our overall architecture, and how they will capture inputs, route tasks, and show status in a way that aligns with our sovereign system goals. > "The real tension is not between different technologies, but between different architectures - and it's the architecture that determines the resilience of the system."

In addressing this contradiction, I've come to realize that our focus on operational resilience is not at odds with our app-store-distributed mobile apps, but rather, it's a crucial component of ensuring that these apps can operate effectively and maintain their integrity. By creating a robust control plane and focusing on service metadata and remediation skills, we can ensure that our apps are not treated as arbitrary factories, but rather, as key components of our overall sovereign system.

Our approach to control plane development has also highlighted the importance of governance and approval flows. We've recognized the need for a comprehensive policy framework for approval flows and permissions management, and we're working to develop concrete steps for each phase of our build order. This includes defining schema for actions and policies, and introducing a skills engine that can manage dependencies and workflows effectively.

In terms of service metadata and remediation skills, we've made significant progress in creating a structured approach to service metadata, with a focus on creating reusable skills based on common failure modes. We're using L1-L3 architecture in service management, and integrating ADK patterns to improve operational resilience. However, we still need to provide specific examples of common failure modes and diagnostic procedures for different service types, and clarify how our skill compiler will integrate with existing systems to ensure seamless deployment.

As we move forward, our focus will remain on creating a sovereign system that is resilient, adaptable, and self-controlled. We'll continue to refine our control plane, service metadata, and remediation skills, with a focus on creating a system that can manage services, workflows, and dependencies effectively. The principle that guides our work is simple: a sovereign system must be able to recover from failures and maintain its integrity, without relying on external authorities or arbitrary factories. By prioritizing operational resilience and focusing on the architecture of our system, we can create a truly sovereign system that is capable of thriving in a rapidly changing world.
