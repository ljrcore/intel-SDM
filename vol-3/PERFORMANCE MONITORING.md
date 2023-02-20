# PERFORMANCE MONITORING

一个名词

PMU (Performance Monitoring Unit)

两个网址

- Performance monitoring events

https://perfmon-events.intel.com

- performance monitoring event files

https://download.01.org/perfmon

## 1. 性能监控概述

三种非架构性（特定型号，不同处理器之间不兼容）性能监控的处理器：

- Pentium处理器

引入一组特定型号性能计数器MSRs用于性能监控，性能计数器的值可以用来优化系统和编译器的性能。

- Intel P6系列处理器

加强性能检测机制，扩展性能事件。

- Intel NetBurst微架构处理器

引入一种分布式的性能监控机制和性能事件。

Intel Core Solo（独显）和Intel Core Duo（多核）处理器支持一组架构性能事件和一组非架构性能事件。新一代的Intel处理器支持增强的架构性能事件和非架构性能事件。从Intel Core Solo和Intel Core Duo处理器开始，有两类性能监控功能。

- 架构性能监控
  - 计数或基于中断的事件采样方法
  - 体系结构无关
  - 可用性能事件数量较少，可通过CPUID.0AH查看

- 非架构性能监控
  - 计数或基于中断的事件采样方法
  - 体系结构相关
  - 不同架构可用性能事件不同，不能通过CPUID查看

## 2. 架构性能监控

架构性能事件可以在不同处理器上使用，CPUID.0AH叶为每个增强功能提供版本ID，高版本兼容低版本功能。

| version ID | Support processor                                            | 
| ---------- | ------------------------------------------------------------ |
| 1          | Intel Core Solo、Intel Core Duo                              |
| 2          | Intel Core 2 Duo processor T7700 、newer processors based on Intel Core microarchitecture |
| 3          | 45 nm and 32 nm Intel Atom processors、Intel Atom Intel Atom processors based on the Silvermont microarchitecture、Intel Atom processors based on the Airmont microarchitecture、Intel Core processors and related Intel Xeon processor families based on the Nehalem through Broadwell microarchitectures |
| 4          | Intel Atom processors based on the Goldmont、Goldmont Plus microarchitectures、Intel processors based on the Skylake through Coffee Lake microarchitectures |
| 5          | Intel Atom processors starting with processors based on the Tremont microarchitecture、Intel processors starting with processors based on the Ice Lake microarchitecture | 

### 2.1 架构性能监控version 1









