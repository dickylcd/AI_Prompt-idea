# Platform Engineering Study Guide: Newbie to Expert

*Based on "Platform Engineering" by Camille Fournier and Ian Nowland*

## Table of Contents
1. [Foundations (Newbie Level)](#foundations-newbie-level)
2. [Intermediate Concepts](#intermediate-concepts) 
3. [Advanced Practices](#advanced-practices)
4. [Expert-Level Implementation](#expert-level-implementation)
5. [Key Definitions & Glossary](#key-definitions--glossary)
6. [Practice Questions](#practice-questions)
7. [Study Checklist](#study-checklist)

---

## Foundations (Newbie Level)

### What is Platform Engineering?

**Core Definition**: Platform engineering is the discipline of developing and operating platforms to manage overall system complexity and deliver leverage to the business through software-based abstractions that serve application developers.

**Key Components**:
- **Platform**: A foundation of self-service APIs, tools, services, knowledge, and support arranged as a compelling internal product
- **Leverage**: Work of few engineers reduces work of greater organization
- **Product Approach**: Customer-centric development with deliberate curation

### The Four Pillars of Platform Engineering

1. **Product**: Taking a curated product approach
   - Building paved paths (easy workflows for common use cases)
   - Creating railways (filling meaningful gaps for broad needs)

2. **Development**: Developing software-based abstractions
   - Platform services and APIs
   - Thick clients when needed
   - OSS customizations
   - Metadata integrations

3. **Breadth**: Serving a broad base of application developers
   - Self-service interfaces
   - User observability
   - Guardrails for safety
   - Multitenancy support

4. **Operations**: Operating as foundations for business
   - Full platform operational responsibility
   - User support systems
   - Operational discipline

### Why Platform Engineering Matters

**The Over-General Swamp Problem**:
- Cloud and OSS create complexity through "glue" code
- Each team making independent choices creates architectural mess
- Maintenance overhead grows exponentially
- Platform engineering provides abstraction and encapsulation

**Benefits**:
- Reduces per-application glue
- Centralizes migration costs
- Enables "you build it, you run it" model
- Creates leverage through shared expertise

### Study Tasks for Newbies:
- [ ] Understand the difference between IaaS vs PaaS
- [ ] Learn what "glue" means in platform context
- [ ] Identify the four pillars in any platform you use
- [ ] Map your current development workflow to platform concepts

---

## Intermediate Concepts

### Getting Started with Platform Teams

**When to Start Platform Engineering**:
- Small Scale (50-250 people): Foster cooperation through lightweight processes
- Medium Scale: Create formal platform teams when cooperation fails
- Large Scale: Transform traditional infrastructure teams

**Team Composition - The Four Key Roles**:

1. **Software Engineers**
   - Systems-interested backend developers
   - Comfortable with on-call responsibilities
   - Ship at deliberate pace

2. **Systems Engineers** 
   - Broad systems knowledge
   - Automation and infrastructure integration
   - Bridge between software and operations

3. **Reliability Engineers**
   - Focus on incident management and SLOs
   - Drive reliability across organization
   - Specialized in operational excellence

4. **Systems Specialists**
   - Deep expertise in specific areas (networking, performance, security)
   - Hire only when clear need exists

### Platform as a Product

**Product Culture Fundamentals**:
- Focus on customers, not just stakeholders
- Understand revealed vs expressed preferences
- Develop customer empathy across entire team

**Product Discovery Process**:
- **Assimilate and Expand**: Take successful prototypes from other teams
- **Partner to Prototype**: Embed with teams to understand problems
- **Realistic Adoption Paths**: Consider migration costs and change budgets

**Avoiding the Feature Shop Trap**:
- Don't just triage feature requests
- Look for patterns that can be generalized
- Enable self-service rather than bespoke implementations

### Operating Platforms

**On-Call Practices**:
- 24x7 coverage for business-critical platforms
- Merged DevOps model (not split SRE)
- Sustainable load: <5 business-impacting pages/week
- Eliminate false alarms

**Support Practices** (by scale):
1. **Stage 1**: Formalize support levels and SLAs
2. **Stage 2**: Separate non-critical support from on-call
3. **Stage 3**: Hire support specialists
4. **Stage 4**: Engineering Support Organization at scale

**Operational Feedback**:
- SLOs and SLAs (error budgets optional)
- Change management processes
- Synthetic monitoring (25% of dev time, 10% of resources)
- Weekly operational reviews

### Study Tasks for Intermediate:
- [ ] Design a hiring plan for a 6-person platform team
- [ ] Create SLOs for a hypothetical platform
- [ ] Practice writing customer empathy interview questions
- [ ] Plan a product discovery process

---

## Advanced Practices

### Planning and Delivery

**Long-Running Project Planning**:

**Proposal Document Structure**:
1. Background, tenets, and guidelines
2. Details of the problem
3. Overview of possible solutions
4. Proposed solution and rationale
5. Plan of action

**Action Plan Elements**:
- Testing and acceptance criteria
- Dependency analysis
- Headcount estimation
- Adoption driving strategy
- Concrete milestones (monthly for first 12 months)

**Bottom-Up Roadmap Planning**:

**Three Work Pools**:
1. **Keep The Lights On (KTLO)**: <40% of workload
   - On-call incident response
   - Essential user support
   - Critical postmortem items

2. **Mandates**: Top-down requirements
   - Infrastructure migrations
   - Compliance initiatives
   - Strategic business projects

3. **System Improvements**: 
   - Reliability and operability
   - Efficiency and performance
   - Security and compliance

**70/20/10 Model for non-KTLO work**:
- 70% core initiatives (incremental work)
- 20% adjacent innovation (rearchitectures)
- 10% transformational innovation (new platforms)

### Rearchitecting Platforms

**Three Engineering Mindsets**:
- **Pioneers**: Explore uncharted concepts, fail often, create prototypes
- **Settlers**: Turn prototypes into products, build trust and understanding
- **Town Planners**: Industrialize and optimize for scale and efficiency

**Why Rearchitecture vs V2**:
- V2 suffers from second-system effect
- Rearchitecture limits customer-visible changes
- Works better with settler/town planner mindsets

**Architectural Maturity Stages**:
1. **Scrappy Platform**: Pioneer mindset, low reliability/security, agile features
2. **Scalable Platform**: Settler mindset, operational rigor, balanced requirements
3. **Robust Platform**: Town planner mindset, metric-driven, secure by design

### Security Architecture Integration

**Security by Design Principles**:
- Don't depend on human behavior
- Provide substantial separation from hazards
- Make secure way the faster/easier way

**Platform Security Patterns**:
- Automated testing tools
- Standardized deployment (IaC)
- Configuration management
- Secrets management
- Standard frameworks with built-in protections
- Tenant-isolated architectures

### Study Tasks for Advanced:
- [ ] Write a project proposal using the 5-section format
- [ ] Create a bottom-up roadmap for a real/hypothetical platform
- [ ] Design security guardrails for a platform
- [ ] Plan a rearchitecture strategy

---

## Expert-Level Implementation

### Stakeholder Management

**Power-Interest Grid Analysis**:
- Map stakeholders by influence and interest level
- Develop specific strategies for each quadrant
- Focus on building coalitions and managing expectations

**Communication Strategies**:
- Wins and Challenges biweekly updates
- Clear escalation paths for conflicts
- Data-driven arguments for investments
- Building trust through transparency

### Migrations and Sunsetting

**Migration Planning**:
- Automated migration tools where possible
- Clear timelines with buffer periods
- Customer success metrics
- Rollback procedures

**Sunsetting Strategy**:
- Deprecation announcements with sufficient lead time
- Migration support and tooling
- Clear end-of-life dates
- Alternative solution paths

### Building Platform Culture

**Cultural Elements**:
- Customer empathy as core value
- Operational excellence mindset
- Continuous improvement focus
- Cross-functional collaboration

**Scaling Challenges**:
- Maintaining culture as team grows
- Balancing innovation with stability
- Managing technical debt
- Succession planning for key personnel

### Advanced Metrics and Measurement

**Platform Health Metrics**:
- Customer satisfaction (CSAT/NPS)
- Adoption rates and user engagement
- Time-to-productivity for new users
- Migration overhead costs
- Platform reliability metrics

**Business Impact Metrics**:
- Developer productivity improvements
- Cost savings through standardization
- Reduced time-to-market
- Security incident reduction

### Study Tasks for Expert:
- [ ] Develop a comprehensive stakeholder management plan
- [ ] Create migration playbooks with automation strategies
- [ ] Design culture assessment and improvement programs
- [ ] Build advanced metrics dashboards

---

## Key Definitions & Glossary

**API/Service Level Terms**:
- **SLI**: Service Level Indicator - specific metric used to measure performance
- **SLO**: Service Level Objective - target value for SLI
- **SLA**: Service Level Agreement - contract based on SLOs
- **Error Budget**: Allowed amount of unreliability

**Platform Types**:
- **Paved Path**: Multi-system workflows made easy through opinionated integration
- **Railway**: Custom-built platform filling specific organizational gaps
- **Shadow Platform**: Unofficial platform built by teams to work around limitations

**Operational Terms**:
- **KTLO**: Keep The Lights On - essential operational work
- **Toil**: Repetitive, manual work that scales with system size
- **MTTR**: Mean Time To Recovery
- **Synthetic Monitoring**: Automated testing that simulates user interactions

**Team Structure Terms**:
- **Merged DevOps**: Combined development and operations responsibilities
- **T1/T2 Support**: Tier 1 (basic) and Tier 2 (advanced) customer support
- **On-call Rotation**: Scheduled availability for production issues

**Architecture Terms**:
- **Multitenancy**: Single system serving multiple isolated customers
- **Thick Client**: Client-side software with substantial logic
- **Infrastructure as Code (IaC)**: Managing infrastructure through code
- **Blue/Green Deployment**: Two identical production environments for safe releases

---

## Practice Questions

### Newbie Level Questions:

1. **Multiple Choice**: What are the four pillars of platform engineering?
   a) Product, Development, Breadth, Operations
   b) People, Process, Platform, Performance
   c) Plan, Build, Run, Monitor
   d) Product, Platform, Process, Performance

2. **Short Answer**: Explain the "over-general swamp" problem and how platforms solve it.

3. **Scenario**: Your startup has 30 engineers. Should you start a platform engineering team? Why or why not?

### Intermediate Level Questions:

4. **Case Study**: You're hired to transform a traditional infrastructure team into platform engineering. What are the first three changes you'd make and why?

5. **Design Problem**: Design the support model for a platform serving 200 internal developers across 20 teams. Include escalation paths and staffing requirements.

6. **Analysis**: A platform team reports 15 pages per week and 50% turnover. Diagnose the problems and propose solutions.

### Advanced Level Questions:

7. **Strategic Planning**: Create a 2-year roadmap for rearchitecting a monolithic platform to microservices while maintaining 99.9% uptime.

8. **Product Management**: Your platform has low adoption despite being mandated. Stakeholders are upset. How do you diagnose and fix the problem?

9. **Architecture**: Design security guardrails for a multi-tenant data processing platform handling sensitive customer data.

### Expert Level Questions:

10. **Organizational Design**: You're building platform engineering for a 5000-person engineering organization. Design the team structure, reporting relationships, and success metrics.

11. **Crisis Management**: A critical platform migration failed halfway through, affecting 60% of production systems. Outline your recovery plan and post-incident improvements.

12. **Strategic Vision**: The CEO wants to reduce infrastructure costs by 40% while improving developer productivity by 30%. Create a 3-year platform strategy to achieve both goals.

---

## Study Checklist

### Foundation Knowledge ✓
- [ ] Understand platform engineering definition and value proposition
- [ ] Know the four pillars and can explain each
- [ ] Recognize the over-general swamp problem
- [ ] Distinguish between platforms, tools, and infrastructure

### Team Building ✓
- [ ] Design balanced platform teams with right skill mix
- [ ] Create hiring processes for different engineering roles
- [ ] Understand management practices for platform teams
- [ ] Plan organizational transformation strategies

### Product and Operations ✓
- [ ] Apply product management techniques to internal platforms
- [ ] Design sustainable on-call and support models
- [ ] Implement operational feedback loops
- [ ] Create customer empathy programs

### Advanced Implementation ✓
- [ ] Plan and execute long-running platform projects
- [ ] Design rearchitecture strategies
- [ ] Implement security by design
- [ ] Create comprehensive measurement systems

### Leadership and Strategy ✓
- [ ] Manage complex stakeholder relationships
- [ ] Plan migrations and sunsetting strategies
- [ ] Build and maintain platform culture at scale
- [ ] Align platform work with business objectives

### Practical Application ✓
- [ ] Can write effective project proposals
- [ ] Create realistic roadmaps and delivery plans
- [ ] Design metrics and measurement systems
- [ ] Handle crisis situations and organizational challenges

---

## Recommended Study Approach

**Phase 1 (Weeks 1-2): Foundation**
- Read Part I of the book thoroughly
- Complete newbie-level practice questions
- Map current organization to platform concepts

**Phase 2 (Weeks 3-6): Core Practices**
- Study team building and product management chapters
- Practice designing team structures and support models
- Complete intermediate-level questions

**Phase 3 (Weeks 7-10): Advanced Topics**
- Focus on planning, architecture, and operations
- Work through complex scenarios
- Attempt advanced-level questions

**Phase 4 (Weeks 11-12): Expert Integration**
- Study stakeholder management and culture building
- Synthesize all concepts into comprehensive strategies
- Complete expert-level questions and case studies

**Ongoing**: Apply concepts in real-world situations, seek mentorship, and continue learning through practice and community engagement.

---

*This study guide provides a structured path from platform engineering newcomer to expert practitioner. Use it alongside the full book text for comprehensive understanding.*