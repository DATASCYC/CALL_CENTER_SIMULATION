# CALL_CENTER_SIMULATION

# Call Center Simulation Project

## Overview

This project aims to simulate a small-scale call center to analyze its operational performance and identify areas for improvement. By modeling customer arrivals, server interactions, feedback handling, and resource utilization, the simulation evaluates key performance metrics such as waiting times, server utilization, customer satisfaction, and feedback analysis efficiency. The insights and recommendations from this analysis are intended to enhance the call center's efficiency and effectiveness in delivering quality service.

## Table of Contents

1. [Project Aim](#project-aim)
2. [Understanding the System](#understanding-the-system)
   - [System Overview: Customers and Servers](#system-overview-customers-and-servers)
   - [Operation Policy](#operation-policy)
   - [Feedback Analysis](#feedback-analysis)
3. [Building the Arena Model](#building-the-arena-model)
4. [Simulation Result Analysis: Understanding Call Center Performance](#simulation-result-analysis-understanding-call-center-performance)
5. [Assumptions](#assumptions)
6. [Limitations](#limitations)
7. [Recommendations](#recommendations)
8. [Comparative Analysis of the New Model Based on Queue Length](#comparative-analysis-of-the-new-model-based-on-queue-length)
9. [Conclusion](#conclusion)

## Project Aim

The goal of this project is to simulate a small-scale call center, model various operational aspects, and analyze key performance metrics. The findings aim to provide insights and recommendations to improve the call center's efficiency and customer service quality.

## Understanding the System

### System Overview: Customers and Servers

- **Premium Customers:** Arrive at 6 calls per hour, with priority service by experienced and rookie servers.
- **Standard Customers:** Arrive at 8 calls per hour, served exclusively by rookie servers.
- **Service Times:** Premium calls follow a Triangular distribution (5, 7, 10 minutes), while Standard calls follow an exponential distribution (mean 3 minutes).

### Operation Policy

- **Wait Time Tolerance:** If a customer's wait time exceeds 10 minutes, the call is escalated to experienced servers, taking an additional 3-5 minutes.
- **Priority Handling:** Escalated calls are prioritized over new Premium calls in the experienced server queue.

### Feedback Analysis

- **Observations:** 50 feedback observations were analyzed using a Triangular distribution for delay times (5.06, 6.09, 9.86 minutes).
- **Feedback Process:** Collected after each call, aiding in service improvement.

## Building the Arena Model

- **Model Design:** The call center model was built to manage incoming calls, prioritize Premium customers, and handle escalations efficiently.
- **Simulation Run:** The model was run for 8 hours with 40 replications to ensure comprehensive performance analysis.

## Simulation Result Analysis: Understanding Call Center Performance

- **Average Waiting Time:** 
  - Rookie server queue: ~0.022 units of time
  - Experienced server queue: ~0.008 units of time
- **Server Utilization:** 
  - Rookie servers: ~32.22%
  - Experienced servers: ~17.17%
- **Customer Experience:** 
  - Premium customers: ~0.012 units of time
  - Standard customers: ~0.025 units of time
- **Call Transfers:** Average of 4.125 calls redirected to experienced servers.

## Assumptions

- **Fixed Arrival Rates:** Constant arrival rates assumed.
- **Modeled Service Times:** Service times estimated with specific distributions.
- **Skill Level Differentiation:** Simplified distinction between experienced and rookie servers.
- **Customer Tolerance:** Fixed waiting tolerance of 10 minutes.
- **Feedback Handling:** All customers provide feedback, analyzed in batches of 15.
- **Lunch Breaks:** Fixed schedules assumed.

## Limitations

- **Random Variable Modeling:** May not reflect real-world variability accurately.
- **Server Utilization:** Fixed number of servers, not adjusted for fluctuating demand.
- **Customer Prioritization:** Simplified prioritization rules.
- **Process Simplifications:** Ignored complex interactions and external factors.
- **Statistical Independence:** Assumes independence among variables.

## Recommendations

- **Dynamic Server Allocation:** Adjust server numbers based on real-time demand.
- **Optimizing Feedback Batch Size:** Increase from 15 to 30 forms for efficient resource utilization.
- **Staggered Feedback Analysis:** Start analysis as soon as a minimum threshold is reached.

## Comparative Analysis of the New Model Based on Queue Length

- **Revised Model Metrics:**
  - Rookie server queue waiting time: ~0.0280 minutes
  - Experienced server queue waiting time: ~0 minutes
  - Rookie server utilization: ~42.48%
  - Experienced server utilization: ~0.68%
  - Premium customer waiting time: ~0.0162 minutes
  - Standard customer waiting time: ~0.0363 minutes
  - Calls redirected: ~6.1 calls

## Conclusion

The simulation provided valuable insights into the call center's operational performance, highlighting areas for improvement. Implementing dynamic server allocation, optimizing feedback batch sizes, and adopting a staggered feedback analysis approach can significantly enhance the call center's efficiency and customer satisfaction. Continuous monitoring and optimization are essential for achieving optimal performance.

<img width="762" alt="Screenshot 2024-05-08 200336" src="https://github.com/DATASCYC/CALL_CENTER_SIMULATION/assets/171361914/f1bd0c36-bacb-4ec7-80d2-5ddc9f881f53">
<img width="570" alt="Screenshot 2024-05-09 075607" src="https://github.com/DATASCYC/CALL_CENTER_SIMULATION/assets/171361914/7ad173b0-8909-4f3b-8364-44b5d37568ea">

