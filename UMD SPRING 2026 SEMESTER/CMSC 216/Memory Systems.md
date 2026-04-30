---
tags: CMSC_216
created: 2026-4-17
description: 4/14, 4/16, 4/21 notes
---

### Measuring Time in Code

The `clock()` function returns the current CPU moment. To measure the CPU time, measure the difference in time between two processes and convert to seconds.

The `gettimeofday()` function measures the wall (real) time by filling a `struct timeval` with info on the time of day.

### Time and Throughput

The total time to complete a function is simply just the CPU time (measured using the `clock()` function).

The **throughput** is the rate of production per unit of time, calculated by dividing the work in progress by the cycle time.

The larger the memory stride (distance between accessed memory locations), the slower the time and lower the throughput. This is because the data may be on different cache lines, so it is not accessed as efficiently as a unit stride (contiguous data, on the same cache line).

### CPU vs. Memory Speed

Before, CPU chips and memory chips ran at similar speeds. The CPU had very little data stored in it, and would fetch data from the memory, do arithmetic, and store back to the memory.

Today, CPU chips run much faster than memory chips.

**Registers** and **cache** were developed in response to the growing speed difference between CPU and memory chips.

Registers can be directly controlled by programmers (in [[Assembly Basics and x86-64|Assembly]]).

Cache memory is mostly managed by the hardware itself, the **Main Memory System**.

### Cache Favors Temporal and Spatial Locality

Example code:
```
for (int i = 0; i < len; i++) {
	sum += array[i];
}
```

The above code exhibits two memory locality features:
1. **Temporal Locality**: Memory recently used likely to be used again soon (like `sum` and `i` used in every loop iteration)
2. **Spatial Locality**: Nearby addresses to recently used memory likely to be used (like `arr[0]` first, then `arr[1]`, `arr[2]`, etc.)

Code that utilizes cache well will run faster.

### Numbers Everyone Should Know

Main memory is comprised of many different physical devices that work together and have differing sizes/speeds.

Accessing memory at an address may involve several levels of cache memory on the CPU (called SRAM), DRAM memory on separate chips, and/or permanent storage (SSDs and HDDs).

|Reference|Time|Analogy
|-|-|-
|Register|-|Your brain
|L1 cache reference|0.5 ns|Your desk
|L2 cache reference|7 ns|Neighbor's desk
|DRAM memory reference|100 ns|This room
|Disk seek|10,000,000 ns|Salt Lake City

### Flavors of Permanent Storage

Memories like cache are fast, small, and **ephemeral** (meaning when powered down, all bits become 0).

There are other memories that are slow but large, and may contain copies of what is in higher parts of the memory pyramid.

These are **persistent**, meaning when they are powered off, they retain information.

Permanent storage is often referred to as a "drive".

##### Hard Disk Drives (HDDs)

- Rotating disk
- Store bits "permanently" as magnetized areas on special platters
- Magnetic disks: moving parts, so HDDs are slow
- Cheap per GB of space

> [!info] Features of Interest of HDDs
> Measures of Quality:
> - Capacity: Bigger is usually better
> - Seek time: Delay before a head assembly reaches an arbitrary track of the disk that contains data
> - Rotational latency: Time for disk to spin around to correct position (faster rotation = lower latency)
> - Transfer rate: Once correct read/write position is found, how fast data moves between disk and RAM
> 
> Sequential vs. random access
> - Sequential reads/writes comparatively fast
> - Random reads/writes comparatively very slow

##### Solid State Drives (SSDs)

- No moving parts, so SSDs are faster
- Most use "flash" memory, non-volatile circuitry
- Major drawback: Limited number of *writes*, disk wears out eventually
- Reads faster than writes
- Sequential somewhat faster than random access
- Expensive

##### Tape Drives

- Slowest (store bits as a magnetic field on a piece of "tape")
- Extremely cheap per GB so mostly used in backup systems

### Terminology

**Bus**: Collection of wires which allow communication between parts of the computer

**Bus speed**: Frequency of the clock signal on a particular bus, usually different between components/buses requiring interface chips

**Interface/Bridge**: Computing chips that manage communications across the bus possibly routing signals to correct part of the computer and adapting to differing speeds of components

**Motherboard**: A printed circuit board connects to connect the CPU to RAM chips and peripherals, and has buses present on it to allow communication between parts