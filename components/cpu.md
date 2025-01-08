# Central Processing Unit (CPU)

<!-- Be as concise and precise as possible, maintaining a technical, rijgorous, scientific tone -->
 
A CPU executes instructions.

## Parameters

<!-- every section should explain what the parameter is, some typical ranges,
and pros/cons changes as you vary the parameter -->

### Core Count

A CPU core is a physical processing unit within the CPU. 2 (low), 4, 6, 8, 16 (high) are typical for personal computers.

Adding cores improves performance for multitasking and parallel processing tasks.

#### Pros

- Increases parallel processing capabilities.
- Enhances multitasking performance.

#### Cores

- More cores can lead to increased power consumption and heat output.
- Not all applications can take full advantage of multiple cores.

### Thread Count

The number of threads refers to the number of sequences of programmed instructions that a CPU can handle at once.
Typical ranges are similar to core counts, with threads usually being double those of cores.

#### Pros

- Allows better utilization of CPU resources through multi-thread application code.

#### Cons

- Threading may not benefit all applications, especially single-threaded ones.
- More threads can also increase complexity in task scheduling and management.

### Performance Core Clock

A CPU cycle is the interval between two successive transitions of the CPU's clock signal (e.g., rising edges). The clock signal is a periodic waveform that synchronizes the activities of the CPU's components. The cycle time is the inverse of the frquency.

The performance core clock measure of how many cycles a CPU can complete per second (clock speed), typically measured in gigahertz (GHz). Typical ranges for consumer CPUs are between 2.5 GHz and 4.5 GHz.

#### Pros

- Higher core clocks can improve the performance of single-threaded applications.
- Faster execution of instructions per clock cycle.

#### Cons

- Increased heat output can require better cooling solutions.
- Higher power consumption.

### Performance Core Clock Boost

The performance core clock boost refers to the temporary increase in the CPU's clock speed above its base frequency when demand is high.

#### Pros

- Provides extra performance for demanding tasks without constantly consuming high power.
- Increases responsiveness during peak loads.

#### Cons

- Boosting can lead to increased heat and power usage.
- May reduce CPU lifespan if thermal conditions aren’t managed properly.

### Socket

The CPU socket is the physical interface between the CPU and motherboard, determining compatibility.

#### Typical Values

- PGA (Pin Grid Array): In a PGA setup, the pins are located on the CPU itself. The socket consists of holes that accommodate the CPU's pins.  Typically used by AMD (e.g., AM4 socket). Easier to replace or upgrade CPUs since the motherboard socket is usually less prone to damage if a pin bends. Bent pins can be difficult to repair or replace. CPUs are more vulnerable due to exposed pins. Examples are AM4, AM5.

- LGA (Land Grid Array): In an LGA setup, the pins are located in the socket rather than on the CPU. The CPU has flat pads that contact the pins in the socket. Primarily used by Intel (e.g., LGA 1200). CPUs have a smooth surface without pins, reducing the risk of damage during handling. Generally regarded as more durable in terms of CPU installation/removal. Damage to the socket often means motherboard replacement, as the pins are fragile and difficult to repair. Refers to the flat contact pads on the CPU that connect with pins in the socket. Examples are LGA 1200, LGA 1700

- BGA (Ball Grid Array): Found in embedded systems and laptops, where the CPU is soldered directly onto the motherboard, offering a compact design. Ball refers to solder balls that connect the CPU to the motherboard.

#### Pros

- Determines motherboard compatibility and upgrade paths.
- Standardized interfaces allow for easier component interchangeability.

#### Cons

- Changing sockets may necessitate a motherboard upgrade.
- Limited backward compatibility with older CPUs.

### Instruction Set Architecture (ISA)

A CPU executes instructions. What "instructions" a cpu can operate on are the "Instruction Set Architecture" (ISA).
This is its "public interface", e.g. affects the behavior of a compiler. These instructions are stored outside the CPU.

#### Typical Values

Two examples are:

- x86 (CISC): Complex Instruction Set Computing allows for more complex, multi-step instructions (e.g., PUSH, POP, or string manipulations).
- ARM (RISC): Reduced Instruction Set Computing focuses on simpler, faster instructions (e.g., basic arithmetic or data moves).

### Microarchitecture

"Microarchitecture" is a high level grouping of CPUs based on how it decomposes instructions into "Micro-Operations" (uOps)

The CPU further breaks down these "instructions" into . These uOPs depend on the "Microarchitecture", which is the physical design that implements the ISA. The uOps are determined at "design time". These uOps are further decomposed into execution units. This decomposition is determined at runtime. Moreover, the execution order of uOps is determined at runtime, varying according to resource constraints.

### IPC (Instructions Per Cycle)

IPC measures the number of instructions a CPU can execute in one clock cycle. It captures efficiency more than raw speed.

#### Typical Ranges

- Lower: 1 - 2 (simple tasks)
- Higher: 3 - 4+ (advanced tasks)

#### Pros

- Higher IPC can result in better performance without increasing clock speed.
- Enhanced efficiency in executing tasks.

#### Cons

- Not all applications will fully utilize higher IPC potential.

### Cache Size

Cache memory is a small-sized type of volatile computer memory that provides high-speed data storage and access to a processor. It stores copies of frequently accessed data or instructions to improve processing speed.

#### L1 Cache

The L1 (Level 1) cache is the fastest type of cache and is located on the CPU chip itself. It typically stores a small amount of data.

- **Typical Sizes**: 32KB to 128KB per core
- **Access Speed**: Fastest with 1-2 cycles latency

The size is determined by microarchitecture

#### Pros

- Extremely quick access which accelerates processor operations.
- Directly integrated into the CPU, minimizing latency.

#### Cons

- Limited size due to cost and chip area constraints.

#### L2 Cache

L2 (Level 2) cache is larger than L1 and can be located on the CPU chip or a separate chip close to the CPU.

- **Typical Sizes**: 256KB to 1MB per core
- **Access Speed**: Moderately fast with 5-10 cycles latency

This is not determined by the microarchitecture.

#### Pros

- Provides more storage than L1 while still being relatively quick.
- Can serve as a buffer between L1 and the slower main memory.

#### Cons

- Slower than L1 but faster than L3; still limited by size constraints.

#### L3 Cache

L3 (Level 3) cache is the largest and typically shared across all CPU cores, residing further from the core than L1 and L2 caches.

- **Typical Sizes**: 4MB to 32MB shared
- **Access Speed**: Slowest among the caches with 20-30+ cycles latency

#### Pros

- Provides a larger capacity to support more data and instructions.
- Helps reduce the time to fetch data from the main memory.

#### Cons

- Slower access compared to L1 and L2.
- Increased complexity and power consumption.

### Cache Latency

Cache latency refers to the delay before data can be accessed from the cache memory.

#### Typical Ranges

- L1: 1-2 cycles (very low latency)
- L2: 5-10 cycles
- L3: 20-30+ cycles (higher latency)

#### Pros

- Lower latency improves data retrieval speed, boosting performance.
- Helps in maintaining fast CPU operations.

#### Cons

- Lowering latency often requires sophisticated, costly hardware design.
- Tapid changes in access patterns can reduce effectiveness.

### Cache Bandwidth

Cache bandwidth is the rate of data transfer between the CPU and cache memory, typically measured in GB/s.

#### Pros

- Higher bandwidth supports faster data processing.
- Benefits applications with large data throughput demand.

#### Cons

- Increasing bandwidth may lead to increased power consumption.
- Complexity in managing high-speed data transfer can increase.

### uOps Throughput

uOps (Micro-Operations) throughput is the number of micro-operations executed per second.

#### Pros

- Higher throughput offers better performance in complex instruction handling.
- Can enhance parallel execution capabilities.

#### Cons

- More uOps may increase the complexity of CPU design.
- High throughput may lead to higher power usage.

### Power Efficiency

Power efficiency measures the ratio of performance gained per watt of power consumed by the CPU.

#### Pros

- Improved efficiency reduces energy costs and environmental impact.
- Can lead to better battery life in portable devices.

#### Cons

- Achieving high power efficiency may require trade-offs with raw performance.
- Technology improvements needed can be costly.


### Chipset Compatibility

A chipset is a collection of controllers and chips on a motherboard that manage communication between the CPU, memory, storage, peripherals, and other components. It determines the features, connectivity options, and compatibility of the motherboard with the CPU and other devices. Chipsets are designed to work with specific CPU families or generations.

#### Typical Chipsets

- **Intel**: Z590, B560
- **AMD**: B550, X570

#### Pros

- Enables full use of CPU features and potential.
- Supports expanded connectivity and advanced motherboard features.

#### Cons

- Limited by motherboard selection.
- May require updates or upgrades for newer technologies.

### Power Requirements (TDP)

The Thermal Design Power (TDP) defines the maximum heat output a CPU is capable of generating under workload. It helps determine the cooling solutions required to manage thermal output.

#### Typical TDP Values

- Low-power CPUs: 15W to 35W
- Mid-range CPUs: 65W to 95W
- High-performance CPUs: 105W and above

#### Pros

- Helps calculate appropriate cooling solutions.
- Provides an estimate of power consumption under normal conditions.

#### Cons

- Higher TDP can lead to increased cooling costs.
- Influences energy consumption and cooling design constraints.
