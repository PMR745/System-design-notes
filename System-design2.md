# System Design Basics — Horizontal vs Vertical Scaling (Gaurav Sen)

## 1. From Code to System

### 1.1 Local Code Execution
- Initially, code runs on a single machine
- Takes input → processes → returns output

### 1.2 Making Code Accessible
- Expose functionality via **APIs**
- Users interact through HTTP requests

### 1.3 Hosting the Application
- Instead of running locally, deploy on:
  - Cloud platforms (AWS, GCP, Azure)
- Benefits:
  - Reliability
  - Scalability
  - Managed infrastructure

---

## 2. Need for Scalability

### Problem:
- Increasing number of users
- Single machine cannot handle all requests

### Goal:
- Handle more requests efficiently
- Maintain performance under load

---

## 3. Vertical Scaling (Scaling Up)

### Definition:
- Increase resources of a single machine
  - CPU
  - RAM
  - Storage

### Characteristics:
- Single powerful server
- No distribution of load

### Advantages:
- Simple to implement
- No need for load balancing
- Faster communication (no network overhead)

### Limitations:
- Hardware limit exists
- Expensive
- Single Point of Failure (SPOF)

---

## 4. Horizontal Scaling (Scaling Out)

### Definition:
- Add multiple machines to handle load

### Characteristics:
- Requests distributed across servers
- Parallel processing

### Advantages:
- Highly scalable
- Fault tolerant (if one server fails, others continue)
- Cost-effective at scale

### Challenges:
- Requires load balancing
- Increased system complexity
- Network communication overhead

---

## 5. Horizontal vs Vertical Scaling

| Feature | Vertical Scaling | Horizontal Scaling |
|--------|----------------|-------------------|
| Approach | Bigger machine | More machines |
| Scalability | Limited | High |
| Complexity | Low | High |
| Fault Tolerance | Low | High |
| Cost | Expensive at scale | More flexible |
| Performance | Faster (no network calls) | Slight overhead |

---

## 6. Load Distribution

- In horizontal scaling:
  - Requests must be distributed across servers
- Achieved using:
  - Load Balancers

### Purpose:
- Prevent server overload
- Ensure efficient utilization of resources

---

## 7. Trade-offs in Scaling

System design is about making trade-offs:

### Vertical Scaling:
- Better consistency
- Simpler architecture
- Limited growth

### Horizontal Scaling:
- Better availability
- Higher scalability
- Increased complexity

---

## 8. Practical Considerations

### 8.1 Real-world Systems
- Use a combination of:
  - Vertical scaling (initial stages)
  - Horizontal scaling (as system grows)

### 8.2 Failure Handling
- Horizontal systems handle failures better
- Redundancy improves reliability

### 8.3 Performance Impact
- Horizontal scaling introduces:
  - Network latency
  - Coordination overhead

---

# Additional Insights (Important for Interviews)

## 1. Always Start Simple
- Begin with single server design
- Scale only when required

---

## 2. Identify Bottlenecks
- CPU
- Memory
- Network
- Database

Scaling decisions depend on bottlenecks

---

## 3. Horizontal Scaling is Default in Modern Systems
- Used by companies like:
  - Google
  - Amazon
  - Netflix

---

## 4. Trade-off Thinking is Key
- No perfect solution
- Choose based on:
  - Scale
  - Budget
  - Requirements

---

## 5. Interview Perspective

When asked:
"How will you scale this system?"

Expected approach:
1. Start with single server
2. Identify limitations
3. Move to horizontal scaling
4. Add load balancing
5. Discuss trade-offs

---

# Summary

- Systems start with a single machine
- Growth introduces scalability challenges
- Two main approaches:
  - Vertical scaling (simple, limited)
  - Horizontal scaling (complex, scalable)
- Real-world systems use a hybrid approach
- Understanding trade-offs is critical in system design
