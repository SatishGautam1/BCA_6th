### The InetAddress Class
- Creating New InetAddress Objects, Getter
### The 'InetAddress' Class in Java
The 'InetAddress' class in java is used to represent an IP address. It can be either an IPv4 or IPv6 address. The class provides various methods to create 'InetAddress' objects and to retrieve information from  them.

#### Creating New 'InetAddress' Objects
To create 'InetAddress' objects, we can use several static methods provided by the class. These methods are:
1. 'getByName(String host)':
	- This method returns an 'InetAddress' objects for the given hostname or IP address string.
	- InetAddress address = InetAddress.getByName("www.example.com");
2. 'getAllByName(String host)':
	- This method returns an array of 'InetAddress' objects for the given hostname. This is useful when a host has multiple IP addresses.
	- InetAddress[] addresses = InetAddress.getAllByName("www.example.com");
3. 'getByAddress(byte[] addr)':
	- This method returns an 'InetAddress' object for the given raw IP address in byte array form.
	- byte[] ipAddr = new byte[] {127, 0, 0, 1};
	- InetAddress address = InetAddress.getByAddress(ipAddr);

