---
title: RAID
created: 2025-12-13
tags:
  - filesystem
aliases:
  - Redundant Array of Independent Disks
lang:
url: https://www.youtube.com/watch?v=Eoaok8mG1vw
---
> [!tldr]
> **RAID** (Redundant Array of Independent Disks) is a storage technology that **combines multiple physical drives into one or more logical units** to improve data reliability, performance, or both, by spreading data across disks using techniques like **mirroring** (copying data) or **striping** (splitting data)

RAID  devices are virtual devices created from two or more real block devices. This allows multiple devices (typically disk drives or partitions thereof)  to be  combined  into  a single device to hold (for example) a single [[Файлова система|filesystem]]. Some RAID levels include redundancy and so can survive some degree  of  device failure.

## Terminology

- **Striping** = in multiple devices but represent in logical single drive

- **Mirroring** = each drive in RAID have the same data (e.x. 5 drives =all 5 have same data)

- **Parity**  = represent something that can be used to rebuild missing data (how many drives fails)