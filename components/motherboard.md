# Motherboard

<!-- Be as concise and precise as possible, maintaining a technical, rijgorous, scientific tone -->
 
Connects and integrates all hardware components.

## Parameters

<!-- every section should explain what the parameter is, some typical ranges,
and pros/cons changes as you vary the parameter -->

### Chipset

A chipset on a motherboard manages data flow between the processor, memory, and peripheral devices. It defines capabilities such as CPU support, overclocking potential, and expandability. This determines the set of features, capabilities, and technologies supported by the motherboard. It includes things like PCIe lanes, SATA ports, USB types, overclocking support, etc.

While socket and chipset are coupled in terms of motherboard design and CPU compatibility, the chipset adds a layer of functionality on top of what the socket physically supports.

#### Typical Values

1. **Intel Chipsets**
   - **Z-Series**: Supports overclocking, multiple GPUs, and high-end features for enthusiasts.
   - **H-Series**: Offers a balance between performance and value, suitable for mainstream users.
   - **B-Series**: Entry-level option, with limited features, suitable for budget builds.

2. **AMD Chipsets**
   - **X-Series**: Provides high-end features, suitable for gaming and overclocking.
   - **B-Series**: A balanced choice, offering a good mix of features and performance.
   - **A-Series**: Cost-effective, suitable for entry-level systems with fewer features.

#### Pros

- Defines the range of supported CPUs and features.
- Influences the overall performance and capabilities of the system.
- Facilitates various connectivity and expansion options.

#### Cons

- Limits upgrade paths to compatible CPUs and features.
- High-performance chipsets can increase overall system cost.
- Requires careful selection based on processing and usage needs.

### Form Factor

The form factor of a motherboard defines its size, shape, and the layout of components and connectors. It determines compatibility with cases and influences the number of expansion slots and ports available.

#### Typical Values

1. ATX
   - Standard size for most desktop motherboards, measuring approximately 305mm x 244mm.
   - Offers the most expansion slots, RAM slots, and generally more features.

2. Micro-ATX (mATX)
   - Smaller than ATX, roughly 244mm x 244mm.
   - Sacrifices some expansion slots but fits smaller cases, suitable for budget builds.

3. Mini-ITX
   - Very compact form factor, around 170mm x 170mm.
   - Limited to fewer expansion slots and RAM slots but supports portable and space-saving builds.

4. Extended ATX (EATX)
   - Larger than a standard ATX, used in high-end or specialized systems.
   - Provides additional space for more components and features, typical for workstations or enthusiast systems.

#### Pros

- ATX: Offers the most functionality due to more slots and connectors.
- Micro-ATX: Balances features and size, fitting smaller cases without losing key capabilities.
- Mini-ITX: Ideal for compact builds, offers essential functionalities in minimal space.
- EATX: Provides maximum expansion and features, suitable for high-performance setups.

#### Cons

- ATX: Requires a larger case, which may limit its use in compact environments.
- Micro-ATX: Fewer expansion slots compared to ATX, limiting future upgrades.
- Mini-ITX: Highly limited expansion capability, may not support high-end components due to space constraints.
- EATX: Requires larger cases, can be more expensive, and may have compatibility issues with standard ATX cases.

### Memory

A memory slot, also known as a DIMM (Dual Inline Memory Module) slot, is an opening on a motherboard designed to hold RAM (Random Access Memory) modules. These slots determine how much RAM you can install and are critical for system performance. Standard types include DDR3, DDR4, and DDR5, with compatibility varying based on the motherboard's design.

The maximum memory of a motherboard dictates the highest amount of RAM it can support. This depends on the number of memory slots available and the capacity supported per slot. The chipset also influences the memory support and speed.

#### Typical Values

DDR stands for Double Data Rate, a type of memory used in computers where data transfer occurs on both the rising and falling edges of the clock signal. This effectively doubles the data throughput compared to single data rate (SDR) memory. The generation of DDR memory (e.g., DDR3, DDR4, DDR5) signifies improvements in speed, power efficiency, and maximum theoretical capacity.

- **DDR3**
  - Supports capacities typically ranging from 4GB to 32GB per slot, with maximum speeds around 2133 MHz.
  - Found in older motherboard models.

- **DDR4**
  - Supports larger capacities, from 8GB to 64GB per slot, with speeds up to 3200 MHz or higher.
  - Common in current generation motherboards, offering improved efficiency and performance over DDR3.

- **DDR5**
  - Still emerging, with even larger capacities and speeds exceeding 4800 MHz, aiming to provide higher performance and efficiency.
  - Supported on cutting-edge motherboards.

#### Pros

- Higher maximum memory allows for better multitasking and memory-intensive applications.
- Provides the ability to upgrade system memory over time.

#### Cons

- More slots and increased memory capacity generally lead to higher costs.
- Overpopulating slots might affect memory performance due to decreased operating speeds.

### Expansion Slots

Expansion slots allow additional cards, such as graphics or sound cards, to be added to the motherboard. Common types include PCI, PCIe x16, x8, x4, and x1, with PCIe x16 being standard for graphics cards.

The "x<number>" notation in PCI Express (PCIe) slots refers to the number of lanes provided by the slot. Each lane consists of a pair of wires, one for transmitting data and one for receiving. More lanes mean higher potential data transfer rates.

- **'x'**: Stands for "by," indicating multiplication or the number of lanes.
- **'<number>'**: Indicates the total number of data lanes available in the slot.

For example:
- **x1**: The slot has 1 lane for data.
- **x4**: The slot has 4 lanes.
- **x8**: The slot has 8 lanes.
- **x16**: The slot has 16 lanes, typically used for high-bandwidth cards like graphics cards.

#### Typical Values

1. PCI (Peripheral Component Interconnect)

   - An older type of expansion slot, used for adding internal components like modems and sound cards.
   - It has largely been replaced by PCIe but might still be found in older systems.

2. PCI Express (PCIe)
   - A more modern expansion slot type, available in different lane configurations: x1, x4, x8, x16.
   - PCIe x16: Primarily used for graphics cards, providing the highest data throughput.
   - PCIe x1, x4, x8: Used for other types of expansion cards such as network and storage controllers.

3. AGP (Accelerated Graphics Port)
   - A legacy slot type specifically for graphics cards, offering better performance than old PCI.
   - Rarely found on modern motherboards, as PCIe has surpassed it in terms of speed and flexibility.

#### Pros

- Provides flexibility and upgradeability.
- Allows for enhanced graphics and additional functionalities.

#### Cons

- Limited space may restrict the number and type of cards.
- May increase the cost due to needing extra components.

### Socket

A socket on a motherboard is a hardware interface that connects the central processing unit (CPU) to the rest of the computer. It consists of a series of pins or pads (a grid array) that align with connectors on the CPU, allowing it to communicate with other components such as memory, storage, and input/output devices. The socket's design ensures both electrical connectivity and secure physical mounting.

#### Typical Ranges

See [CPU Socket documentation](cpu.md###socket)

#### Pros

- Determines the range of compatible CPUs.
- High-quality sockets support better CPU performance.
- Facilitates easy CPU installation and replacement; standardization allows compatibility across different CPUs and motherboards.

#### Cons

- Limits CPU upgrade options to those compatible with the socket.
- Different sockets require specific heat sinks and coolers.
- Limited to specific CPU types due to socket design

### DIMM Slots

A DIMM (Dual Inline Memory Module) slot on a motherboard is a connector used for installing RAM (Random Access Memory) modules. These slots are crucial for determining the amount and type of memory a system can support, directly influencing system performance and multitasking capability.


#### Typical Values

- Number of Slots: Most motherboards have between 2 to 8 slots, allowing for varying configurations of memory.
- Maximum Capacity per Slot: Typically ranges from 4GB to 64GB, depending on the type of RAM and motherboard support.

#### Pros

- Allows for greater RAM capacity, enhancing multitasking and performance.
- Enables future upgrades by adding more memory modules.

#### Cons

- More memory slots can increase motherboard cost.
- Compatibility constraints based on memory type and motherboard design can limit options.


### Headers

Headers on a motherboard connect to external ports and internal components for power, input/output, and communication. They play a crucial role in interfacing with peripherals and power supply.

#### Typical Values

1. **Power Headers**
   - ATX Power Connector: Provides electrical power from the PSU to the motherboard.
   - CPU Power Connector: Supplies power specifically to the CPU socket.

2. **Fan Headers**
   - CPU Fan Header: Controls CPU cooling fan speed and monitors performance.
   - System Fan Headers: Manage additional case fans for improved airflow.

3. **I/O Headers**
   - USB Headers: Connect front panel USB ports for additional peripheral connectivity.
   - Audio Headers: Link front audio ports for microphone and headphone connections.
   - Front Panel Header: Offers connectivity for power/reset switches and status LEDs.

#### Pros

- Facilitate additional connectivity and control options.
- Enhance system cooling and power management capabilities.
- Support easy customization with additional front panel ports and devices.

#### Cons

- Limited number of headers may restrict component connection options.
- Overburdening headers with multiple devices can lead to power and cooling inefficiencies.
