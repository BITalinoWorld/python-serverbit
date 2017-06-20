# OpenSignals Barebone

The ServerBIT is a barbone example application based on the Twisted event-driven networking engine, and designed to demonstrate the OpenSignals client-server architecture. You can use and modify the source code under the terms of the GPL licence.

This architecture is based on an asynchronous message passing protocol, in which the server and the client communicate using JSON-formatted strings. Although this code is primarily used for BITalino, it is completely general purpose.

ServerBIT receives Python instructions as string-based requests from a client, evaluates them, and replies with the same instruction having the evaluation results as input arguments.

ClientBIT is an example HTML/JS that connects to ServerBIT and opens a connection to a specified BITalino device to acquire data from A3 (ACC data as of early-2014 units) and draw it on the browser in realtime.

In our example, ClientBIT is also prepared to evaluate the strings received from the server as JS instructions.


## Prerequisites

- Python 2.7 or above must be installed;
- BITalino API and dependencies installed;
- PySerial module installed;
- Twisted matrix module installed.

## Testing ServerBIT

- edit `ClientBIT.html` on a text editor and change `'/dev/tty.bitalino-DevB'` to the MAC address or Virtual COM port of your BITalino device;
- launch the `ServerBIT.py` script using your Python interpreter;
- once a message similar to `LISTENING AT 127.0.0.1:9001` appears in the console the server is ready to receive a connection;
- open `ClientBIT.html` on your web browser;
- you should start to see the instruction call log on the page body, and a real time signal corresponding to A3.

## References

H. Silva, A. Lourenço, A. Fred, R. Martins. BIT: Biosignal Igniter Toolkit. Computer Methods and Programs in Biomedicine, Volume 115, 2014, Pages 20-32.


M. Lucas da Silva, D. Gonçalves, T. Guerreiro, H. Silva. A Web-Based Application to Address Individual Interests of Children with Autism Spectrum Disorders. Procedia Computer Science, Volume 14, 2012, Pages 20-27.

## Screenshots

![ServerBIT](https://raw.githubusercontent.com/BITalinoWorld/python-serverbit/master/ServerBIT.png)
![ClientBIT](https://raw.githubusercontent.com/BITalinoWorld/python-serverbit/master/ClientBIT.png)

