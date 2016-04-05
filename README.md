# trickleTWIN
Implementation of the Trickle Algorithm for TWIN node

Using *Multicast Addressing Scheme* `ff02::1` for disseminating code
within an Ad-Hoc network consisting of the following:

Clients:

- __Raspberry Pi 2 Model B__ with __1GB RAM__

- __LogiLink WiFi Adapter__

Server:

- __Ubuntu 14.04 LTS__ Laptop


## Usage

For general Idea:

    python main.py -h or python main.py --help

For Server (Laptop):
	
	python main.py -s /Path/to/File fileName.ihex 
		or 
	python main.py --server /Path/to/File fileName.ihex

For Client (RPis):

	python main.py -r
		or
	python main.py --receiver


## Structure

	-- twinSocket.py : socket class to be used 
	-- trickle.py : Implementation of Trickle Timer taken from [simpleRPL](https://github.com/tcheneau/simpleRPL)
	-- message_constants.py : *pseudo-header* parameters for Version control
	-- Sender/Receiver.py: implementation of server/client respectively

### Dissemination Code

- creating a standard `.ihex` using the [Contiki-OS](https://github.com/contiki-os/contiki) for *Zolerta Z1 nodes*

### Improvements

- add `VERSION` argument to be used when uploading new `.ihex` to network for version-control.
