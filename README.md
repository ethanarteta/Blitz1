# Blitz Exercise Documentation

## Introduction

This documentation provides an overview of a recent blitz exercise conducted on our web server, including the observed performance metrics, the actions taken to resolve the identified issues, and the underlying purpose of the exercise.

### Purpose:
The primary purpose of this blitz exercise was to evaluate the performance of our web server under simulated high load conditions and assess the impact on latency. By doing so, we aimed to:

1. Identify potential bottlenecks and weaknesses in our infrastructure.
2. Evaluate the need for performance optimizations.
3. Test the effectiveness of implementing a Content Delivery Network (CDN) to improve latency.

## Scenario

In this exercise, we simulated a scenario in which our web server experienced a sudden surge in traffic, with 1000 concurrent user requests hitting our server simultaneously.

## Observations

### Initial Scenario (Without CDN):

**Latency:** 
- Average latency: 40ms

**Key Findings:**
- High latency was observed under the simulated high load conditions.
- Response times were slower than desired, potentially leading to a poor user experience.

### Resolution (Implementing CDN):

**Action Taken:**
- Deployed Amazon CloudFront as a CDN to serve content.

**Post-Implementation Observations:**

**Latency:**
- Average latency: Reduced to 7ms

**Key Findings:**
- After implementing the CDN (Amazon CloudFront), latency significantly improved.
- Average response times decreased from 40ms to 7ms, enhancing the user experience.
- Content delivery became more efficient, with cached content serving the majority of requests.

## Actions Taken

1. **Implemented Amazon CloudFront CDN:**
   - Deployed Amazon CloudFront to distribute content to edge locations.
   - Applied CloudFront's caching capabilities to deliver static content frequently requested from edge locations, reducing the load on our web server.

2. **Configured CDN Settings:**
   - Set up proper caching rules and behavior settings within CloudFront to optimize content delivery and reduce latency.
   - Configured appropriate security and access control measures.

3. **Monitoring and Optimization:**
   - Established monitoring and alerting to ensure the CDN's performance and make further optimizations as necessary.
   - Continuously assessed the effectiveness of the CDN in reducing latency and improving the overall user experience.

## Optimization

### Future Optimization Opportunities:

1. **Multiple CDN Servers:**
   - We can consider using multiple CDN servers in different places around the world to make our website faster for users everywhere.
    
2. **Horizontal Scaling with Load Balancer:**
   - Implementing horizontal scaling alongside a load balancer can also help to reduce latency. The load balancer can evenly distribute incoming user traffic across multiple web servers, optimizing response times.

