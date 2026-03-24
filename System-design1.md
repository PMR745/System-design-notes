# System Design Primer — Notes

## 1. What is System Design?

System Design is the process of:
- Converting business requirements into technical solutions
- Designing large-scale distributed systems
- Ensuring scalability, reliability, and maintainability

It involves applying computer engineering principles to build systems that can handle real-world usage.

---

## 2. Key Goals of System Design

A good system should be:

- **Scalable** → Handle increasing users/traffic
- **Reliable** → System should not fail frequently
- **Maintainable** → Easy to update and extend
- **Performant** → Low latency and high throughput

---

## 3. Scaling Concepts

### 3.1 Vertical Scaling
- Increasing the power of a single machine
- Example: Upgrade CPU, RAM

**Pros:**
- Simple to implement

**Cons:**
- Limited by hardware
- Expensive

---

### 3.2 Horizontal Scaling
- Adding more machines to handle load
- Requests distributed across servers

**Pros:**
- Highly scalable
- Fault tolerant

**Cons:**
- Complex system design

---

## 4. Preprocessing (Cron Jobs)

- Tasks that are done in advance
- Example:
  - Data aggregation
  - Report generation

**Purpose:**
- Reduce real-time computation load
- Improve performance

---

## 5. Backup Servers

- Secondary servers that take over if primary fails

**Goal:**
- Improve fault tolerance
- Avoid single point of failure

---

## 6. Microservices Architecture

- Break system into smaller independent services

**Advantages:**
- Independent deployment
- Better scalability
- Easier maintenance

**Trade-off:**
- Increased complexity (network calls, coordination)

---

## 7. Distributed Systems

- System spread across multiple machines

**Key Characteristics:**
- No single machine handles everything
- Components communicate over network

**Challenges:**
- Network failures
- Data consistency
- Synchronization

---

## 8. Load Balancing

- Distributes incoming requests across multiple servers

**Benefits:**
- Prevents server overload
- Improves availability
- Enhances performance

---

## 9. Decoupling

- Reduce dependencies between components

**Example:**
- Using message queues

**Benefits:**
- Easier scaling
- Independent deployments
- Fault isolation

---

## 10. Logging and Metrics

- Collect system data for monitoring

**Examples:**
- Request latency
- Error rates
- Throughput

**Purpose:**
- Debugging
- Performance optimization

---

## 11. Extensibility

- System should support future changes easily

**Example:**
- Adding new features without breaking existing system

---

## 12. Low-Level Design (LLD)

- Focus on implementation details
- Classes, APIs, database schema

**Contrast:**
- High-Level Design → Architecture
- Low-Level Design → Implementation

---

# Additional Insights (Important for Interviews)

## 1. Think in Trade-offs
Every decision involves trade-offs:
- Scalability vs Simplicity
- Consistency vs Availability

---

## 2. Avoid Single Point of Failure
- Always design for redundancy
- Use backups and replication

---

## 3. Start Simple, Then Scale
- Do not over-engineer initially
- Scale when required

---

## 4. Real Goal of System Design Interviews

Not to memorize solutions, but to:
- Break down problems
- Justify decisions
- Communicate clearly

---

## 5. Core Mental Model

User Request → Load Balancer → Servers → Database → Response
Then optimize each layer:
- Add caching
- Add queues
- Add replication

---

# Summary

System Design is about:
- Handling scale
- Designing reliable systems
- Making trade-offs
- Thinking in distributed architecture

It evolves from:
Simple system → Scaled system → Distributed system
