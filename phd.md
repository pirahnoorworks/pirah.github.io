---
layout: default
title: "PhD Research"
---

# PhD Research - Adaptive Runtime Systems for AI Workloads

## Building Adaptive Runtime Systems for AI Workloads

My doctoral research focused on the design of runtime systems that can efficiently execute AI workloads on heterogeneous computing platforms.

The central challenge was understanding how computational workloads should be partitioned, scheduled, and adapted across resources with different compute capabilities, memory characteristics, and performance behaviors.

While convolutional neural networks were used as representative workloads, the research itself concentrated on runtime systems, resource orchestration, performance engineering, scheduling, interference mitigation, and adaptive execution.

The resulting work produced several scheduling and runtime frameworks capable of continuously improving workload placement decisions based on workload behavior and platform characteristics.

---

# Research Vision

Modern computing systems are increasingly heterogeneous.

A single platform may contain:

- Different classes of CPUs
- Multiple memory hierarchies
- Accelerators
- Shared system resources
- Non-uniform communication paths

Traditional execution models typically assume resources are interchangeable.

My research explored a different approach:

Treat hardware differences as an optimization opportunity rather than an inconvenience.

The goal was to design runtime systems that continuously make intelligent decisions about where work should execute and how resources should be utilized.

---

# Runtime Systems Engineering

A major portion of the research involved developing and extending runtime infrastructure.

Rather than only building applications, I worked directly inside runtime systems responsible for task execution, scheduling, resource allocation, tracing, and workload orchestration.

### Key Contributions

- Extended XiTAO runtime internals
- Modified scheduler components
- Developed resource-allocation mechanisms
- Implemented affinity-aware execution
- Designed workload-placement strategies
- Built runtime tracing infrastructure
- Investigated persistent task execution models
- Developed adaptive task scheduling mechanisms

### Core Skills

- Runtime systems development
- Systems software engineering
- Concurrency
- Multithreading
- Resource scheduling
- Runtime observability
- Execution orchestration

---

# Hardware-Aware Scheduling

One of the primary themes throughout the research was hardware-aware scheduling.

The work explicitly considered differences in:

- Processor performance
- Memory bandwidth
- Resource contention
- Hardware asymmetry
- Execution efficiency

Scheduling decisions were based not only on workload characteristics but also on the capabilities of the underlying hardware.

### Topics Explored

- ARM big.LITTLE scheduling
- CPU affinity management
- Execution-place assignment
- NUMA-aware execution
- Resource contention
- Performance asymmetry

### Outcomes

- Improved workload distribution
- Increased throughput
- Better resource utilization
- Reduced bottlenecks
- Improved scalability

---

# Large-Scale Scheduling Optimization

Many scheduling problems quickly become computationally intractable.

The number of possible scheduling configurations often grows into millions of candidate solutions.

My research focused on developing techniques capable of finding high-quality schedules without requiring exhaustive exploration.

### Areas of Work

- Design-space exploration
- Heuristic-guided search
- Evolutionary search
- Runtime autotuning
- Search-space pruning
- Cost-function optimization

### Why It Matters

The same type of optimization problem appears today in:

- AI serving infrastructure
- Resource schedulers
- GPU orchestration systems
- Distributed inference platforms
- Cloud resource allocation systems

---

# PipeSearch

## Online Schedule Optimization Framework

PipeSearch was developed to explore large scheduling spaces while minimizing search cost.

The framework used runtime-aware search mechanisms to efficiently converge toward high-quality scheduling solutions.

### Characteristics

- Runtime optimization
- Guided search
- Adaptive scheduling
- Near-optimal schedule generation
- Reduced search complexity

### Industry Interpretation

Viewed from an infrastructure perspective, PipeSearch is essentially a scheduling optimization engine capable of navigating large execution spaces while continuously balancing performance and resource usage.

---

# Shisha

## Hardware-Aware Resource Orchestration Framework

Shisha extended the ideas introduced by PipeSearch and removed the requirement for large pre-generated scheduling spaces.

Instead, it generated scheduling decisions dynamically and adapted more effectively to increasingly heterogeneous systems.

### Core Capabilities

- Dynamic schedule generation
- Resource-aware execution
- Runtime adaptation
- Workload balancing
- Online optimization

### Modern Relevance

Many concepts from Shisha map naturally to modern infrastructure systems where workloads must be assigned across combinations of:

- CPU
- GPU
- NPU
- Accelerators

while simultaneously balancing performance and resource constraints.

---

# Multi-Pipeline AI Inference

As the research evolved, the focus expanded beyond optimizing individual inference pipelines.

A major challenge emerged when multiple AI pipelines execute concurrently and must share the same system resources.

The problem shifted from:

How should one workload be scheduled?

to:

How should many workloads share infrastructure efficiently?

### Research Topics

- Concurrent inference pipelines
- Multi-workload execution
- Pipeline coordination
- Shared-resource scheduling
- Throughput optimization
- Runtime workload balancing

### Why It Matters

Modern AI serving systems process thousands of concurrent requests sharing the same infrastructure.

The concepts explored during this work are closely related to:

- AI serving platforms
- Multi-tenant inference
- Resource orchestration
- Request scheduling
- Accelerator utilization

---

# Interference Mitigation & Resource Contention

One of the most practical aspects of the research focused on understanding how workloads affect each other when sharing resources.

Many systems fail to achieve expected performance because workload interactions create contention for:

- CPU resources
- Memory bandwidth
- Cache capacity
- Shared execution resources

The research investigated how runtime systems can identify and mitigate these effects.

### Areas Studied

- Resource contention
- Performance interference
- Co-execution effects
- Shared-resource behavior
- Contention-aware scheduling
- Performance isolation

### Key Insight

A perfectly balanced workload does not necessarily produce balanced performance.

Understanding interference became just as important as understanding workload size.

### Relevance Today

This challenge appears throughout modern computing infrastructure including:

- Multi-tenant AI serving
- GPU sharing
- Cloud scheduling
- Resource governance
- Distributed AI systems

---

# Performance Engineering

Performance measurement and optimization formed a central part of the research.

Every scheduling decision required validation through extensive measurement and analysis.

### Tools & Techniques

#### Profiling

- Linux Perf
- PMU counters
- TensorBoard
- Extrae
- Custom instrumentation

#### Analysis

- Roofline analysis
- Throughput analysis
- Latency analysis
- Scalability studies
- Contention analysis
- Memory behavior analysis
- NUMA analysis

### Results

The research produced scheduling decisions driven by measured system behavior rather than assumptions.

---

# Benchmarking & Experimental Infrastructure

A significant amount of engineering effort went into creating benchmarking and experimentation infrastructure.

The objective was to support reliable evaluation across multiple workloads, hardware platforms, and scheduling policies.

### Infrastructure Built

- Experiment automation frameworks
- Benchmark runners
- Cluster execution pipelines
- Structured logging systems
- Data collection workflows
- Result databases
- Visualization pipelines
- Automated analysis systems

### Scale

- Thousands of experiments
- Automated parameter sweeps
- Multi-platform validation
- Large benchmarking campaigns

---

# HPC & Heterogeneous Computing

The research was evaluated across both embedded and high-performance computing environments.

### Platforms

#### Embedded & Edge Systems

- NVIDIA Jetson TX2
- ARM Cortex-A57
- ARM big.LITTLE architectures

#### High Performance Computing

- Intel KNL
- HPC clusters
- SNIC infrastructure
- NAISS infrastructure

### Focus

- Performance portability
- Scalability
- Resource efficiency
- Hardware heterogeneity
- Runtime adaptation

---

# Technical Expertise Developed

### Runtime Systems

- Scheduler development
- Runtime modification
- Resource management
- Task orchestration
- Execution placement

### AI Infrastructure

- Inference optimization
- Multi-pipeline execution
- Adaptive scheduling
- Resource-aware execution
- Runtime decision systems

### Performance Engineering

- Profiling
- Bottleneck analysis
- Scalability analysis
- Performance characterization
- Roofline modeling

### Systems & HPC

- Heterogeneous computing
- Linux systems
- Affinity management
- NUMA optimization
- Parallel execution

### Resource Orchestration

- Workload balancing
- Interference mitigation
- Resource allocation
- Contention-aware scheduling
- Multi-tenant execution concepts

---

# Impact

Although the application domain was AI inference, the broader contribution was the design of adaptive runtime systems capable of intelligently orchestrating workloads across heterogeneous computing resources.

The work evolved from optimizing a single AI pipeline into managing collections of competing workloads sharing limited resources, making it highly relevant to modern AI infrastructure, serving systems, runtime platforms, and large-scale computing environments.

## Summary

Designed adaptive runtime scheduling and resource orchestration systems that optimized single-pipeline and multi-pipeline AI workloads across heterogeneous computing platforms through hardware-aware scheduling, interference mitigation, online optimization, and performance-driven execution.
