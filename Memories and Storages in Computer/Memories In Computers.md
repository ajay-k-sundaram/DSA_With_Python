It is used to store Data and the data is stored by splitting up the memory as bits or binary digits which are called as cells. Each cell has a unique address.

## Units of Memory

8 bits = I byte
1024 (2<sup>10</sup>) bytes = 1 kilo byte
1024 (2<sup>10</sup>) kilo bytes = 1 mega byte (2<sup>20</sup>) bytes
1024 (2<sup>10</sup>) mega bytes = 1 giga byte (2<sup>30</sup>) bytes
1024 (2<sup>10</sup>) giga bytes = 1 tera byte (2<sup>40</sup>) bytes

Processor determines the speed of reading and writing data. Let's take a 2GHz processor.

Frequency = 2GHz
Time = 1 / Frequency = 1/(2 * 10<sup>9</sup>) sec
= 1/2 (10<sup>-9</sup>) sec 
= 1/2 n sec

Higher processing speed requires High amount and high speed storage devices.

![Alt text](https://github.com/ajay-k-sundaram/Notes-for-Computer-Science/blob/master/Memories%20and%20Storages%20in%20Computer/Resources/Memory%20Classifications.png?raw=true)
#### RAM
```
SRAM (Static Random Access Memory)

	It has 6 series of transistors and 0 capacitors. Since it has no capacitors, there will be no power discharge and there is not need to refresh.

	It is hyper fast than DRAM and it will consume low power. 
	It is costly and has low memory capacity.

	Classifications :

		L1 Cache : 2 to 64 KB
		
			Level one Cache is places inside the Processor
				Instruction Cache 
				Data Cache
			L1 cache is the fastest than all.
			
		L2 Cache : 256 to 512 KB

			Level Two Cache can be place either inside or outside the Processor
			It is faster than RAM but not faster than L1.
					
		L3 Cache : 1MB to 8MB

			Level Three Cache will not available on all CPU. It will be available only on some high end processors.
			It will enhance the performance of L1 and L2 Cache.
			It will be placed outside the processors

DRAM (Dynamic Random Access Memory)

	It has many millions of Transistors and Capacitors and each bit stores in a single capacitor and Transistor acts as a switch.
	
	If capacitor has charge    : It is 1
	If capacitor has no charge : It is 0

	If transistor is Open then there is no power flow
	If transistor is Close then power will flow

	DRAM requires periodic refresh.

	Classifications :
	
		ADRAM (Asynchronous Dynamic Random Access Memory)
			Older generation RAM and it is not Syncronous with Processor Clock
			
		SDRAM (Synchronous Dynamic Random Access Memory)
			It is otherwise called Single Data Rate Dynamic Random Access Memory
			It can transfer only one signal in their lifecycle.
			It will operate at 3.3 V
			
		DDR SDRAM (Double Data Rate Synchronous Dynamic Random Access Memory)
			It can transfer two signal in their lifecycle.
			Low consumption of power compared to SDRAM

			Classifications :
			
				DDR1 : 2.5 TO 2.6 V
				DDR2 : 1.8 V
				DDR3 : 1.35 TO 1.5 V
				DDR4 : 1.2 V

	Cache Memory

		It is a type of RAM which placed in Processor
		
	
```

### Stack
```
The stack is a region of memory in the primary memory (RAM) that is used for storing local variables, function call information, and control flow data. It operates in a Last-In-First-Out (LIFO) manner, meaning that the last item added to the stack is the first one to be removed. The stack is typically managed by the compiler or the runtime environment.

When a function is called, a new frame is created on the stack to hold the function's local variables, parameters, return address, and other contextual information. When the function exits, its frame is removed from the stack. This automatic memory management makes the stack memory very efficient for managing local variables and function call operations
```

#### Heap
```
The heap is another region of memory in the primary memory (RAM) used for dynamic memory allocation. Unlike the stack, which has a well-defined and controlled structure, the heap is a pool of memory that can be allocated and deallocated as needed during the program's execution.

In languages like C++, Java, and Python, you can use functions like malloc, new, malloc(), alloc(), or new to allocate memory on the heap. This memory is typically used for storing objects, data structures, and variables that have a longer lifetime than those stored on the stack.

Heap memory requires manual memory management in many programming languages. Developers are responsible for allocating memory when needed and releasing it when it's no longer required (a process known as memory deallocation or freeing memory). Failing to release memory when done can lead to memory leaks.
```

#### ROM 
```
	It is read only and can't write anything.
	It is used form some default system configurations.
		Like BIOS settings, Booting Operations.
	It is pre placed in the Motherboard.
	It's volatility depends on the use case.

	Classifications :

		PROM   : Programable Read Only Memory
			It is one time programable.
			
		EPROM  : Erasable Programable Read Only Memory
			Program can be erased and rewrited using UV light for only one time.
			Erasing time will be morethan 15 min
			It will operate at 12.5V
			
		EEPROM : Electrically Erasable Programmable Read Only Memory
			Can be rewritable using electrical signal.
			Erasing can be done in mili seconds.
			It will operate at 5V.
			Multiple erasing will reduce the quality.
	
```

#### Secondary Storage
```
HDD :
	It will have a aluminum disc with magnetic coating of 10 to 20 nm. 
	Data is stored by magnetizing and demagnetizing the coating.
	The speed depends on the rotating speed of the disc. Now all hard disc have above 4500 rpm.
	Power consumption will be around 6w

SSD :
	Solid State Drives are made up of Silicon micro chips.
	Data is stored uing electric signals in cells.
	Flash Memory technology is used which has special type of transistors to store data.

	RAM has transistors with 3 pins but Flash memory has two gate technology. Hence SSD requires no power to read data.

	Data recovery in SSD is pitty much hard.
	Power Consumption will be around 2 to 3w.

Optical Storages :
	Laser is used to read and write the data.
	It is made up of plastic and metals and its surface is divided into tracks.

	The surface has ups and dows. the downs in CD are called pits and the flat surface or ups are called land. The laser will pass and reflect these pits and lands. the lands will give 1 and pits will give 0.

	High power laser is used to write the data and Low power laser is used to read the data.
	The writing is done by burning the disc the burned area is 0 and the unburned area is 1. 

	Example :
		CD (700 MB), DVD (4.5 to 8.7 GB), Blu-Ray (25 to 50GB). SIngle and Dual layer are available.

	Classifications :

		Read-Only  :
		Recordable :
		Rewritable :
	
	
```


![Alt text](https://github.com/ajay-k-sundaram/Notes-for-Computer-Science/blob/master/Memories%20and%20Storages%20in%20Computer/Resources/Memory.png?raw=true)

![Alt text](https://github.com/ajay-k-sundaram/Notes-for-Computer-Science/blob/master/Memories%20and%20Storages%20in%20Computer/Resources/ASCII%20Table.png?raw=true)
## Data Storage

![Alt text](https://github.com/ajay-k-sundaram/Notes-for-Computer-Science/blob/master/Memories%20and%20Storages%20in%20Computer/Resources/Memory%20Storage.png?raw=true)








