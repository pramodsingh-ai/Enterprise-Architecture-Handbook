# Functional vs Non-Functional Requirements

> "Architects don't build software for requirements alone—they build software that satisfies quality expectations."

---

# Introduction

Every software system is built to satisfy two categories of requirements:

1. Functional Requirements (FRs)
2. Non-Functional Requirements (NFRs)

Many projects successfully implement every functional requirement but still fail in production because the non-functional requirements were never identified or properly addressed.

An experienced architect gives equal importance to both.

---

# What Are Functional Requirements?

Functional requirements describe **what the system should do**.

They define the business capabilities the application must provide.

Examples include:

- Customer registration
- User login
- Loan application submission
- Fund transfer
- Credit card payment
- Generate account statements
- Search customer information

These requirements are directly visible to business users.

---

# What Are Non-Functional Requirements?

Non-functional requirements define **how well the system should perform** while delivering those business capabilities.

Examples include:

- Response time
- Scalability
- Availability
- Reliability
- Security
- Performance
- Maintainability
- Disaster Recovery
- Compliance
- Monitoring

Business users may not explicitly request these, but they are often critical to success.

---

# Enterprise Scenario – NexusBank Platform

The business requests:

> Customers should be able to apply for a personal loan online.

This is a **Functional Requirement**.

However, the architect must ask additional questions.

### Performance

- Should the application load within 2 seconds?

### Availability

- Should the platform operate 24×7?

### Scalability

- How many concurrent users are expected during salary days?

### Security

- Should customer information be encrypted?

### Reliability

- What happens if the credit bureau service becomes unavailable?

These questions define the non-functional requirements.

---

# Comparing FRs and NFRs

| Functional Requirements | Non-Functional Requirements |
|--------------------------|-----------------------------|
| Describe business features | Describe quality attributes |
| Visible to users | Usually invisible to users |
| Define what the system does | Define how the system behaves |
| Often come from business teams | Often discovered by architects |
| Usually easier to validate | Often require performance and operational testing |

---

# Why NFRs Matter

Consider two banking applications.

Both support:

- Login
- Fund Transfer
- Loan Processing

Functionally they are identical.

However:

Application A

- Response Time: 1.5 seconds
- Availability: 99.99%
- Supports 2 million users
- Disaster Recovery in 15 minutes

Application B

- Response Time: 12 seconds
- Frequent outages
- Slow during peak traffic
- No disaster recovery

Both satisfy the same functional requirements.

Only one satisfies the business.

---

# Architect's Responsibility

Architects are responsible for identifying NFRs that stakeholders often forget to mention.

Typical questions include:

- How many users?
- Expected growth?
- Peak traffic?
- Recovery objectives?
- Regulatory requirements?
- Budget constraints?
- Operational support model?
- Required service availability?

The answers directly influence architecture decisions.

---

# How NFRs Influence Technology

Suppose availability must be 99.99%.

Possible decisions include:

- Multiple Availability Zones
- Load Balancers
- Health Checks
- Active-Active Deployment
- Database Replication

Suppose response time must remain below 2 seconds.

Possible decisions include:

- Redis Cache
- CDN
- Database Indexing
- Horizontal Scaling
- Asynchronous Processing

Notice that NFRs determine architecture.

Architecture determines technology.

---

# Common Mistakes

- Ignoring NFR discussions.
- Assuming developers will "optimize later."
- Treating security as a separate phase.
- Designing without capacity estimates.
- Assuming functional testing validates system quality.

---

# Best Practices

- Capture NFRs during requirement gathering.
- Quantify every NFR wherever possible.
- Validate NFRs through testing.
- Review NFRs during architecture discussions.
- Revisit NFRs as business scales.

---

# Architect's Checklist

Before approving a design, ask:

- Have all functional requirements been identified?
- Have non-functional requirements been quantified?
- Can the proposed architecture satisfy expected scale?
- What happens during component failures?
- Have security and compliance requirements been addressed?
- Can the operations team support this solution?

---

# Key Takeaways

- Functional requirements define **what** the system does.
- Non-functional requirements define **how well** it does it.
- Most production failures result from poor handling of NFRs rather than missing functionality.
- Architects should proactively identify NFRs.
- Every major architectural decision should trace back to one or more NFRs.

---

# Summary

Great software is not measured only by the features it delivers.

It is measured by its ability to deliver those features securely, reliably, efficiently, and consistently under real-world conditions.

Understanding the relationship between functional and non-functional requirements is one of the first responsibilities of every Enterprise Architect.