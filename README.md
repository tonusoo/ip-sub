# IP-sub


A small utility to manipulate prefixes. There are other possible solution on npm, this was created mostly to prioritize performance.

It implements the following methods.

* `getIpAndCidr` - if you provide "99.88.77.0/24" it returns ["99.88.77.0", 24]

* `isValidPrefix` - it returns true/false

* `isValidIP` - it returns true/false

* `sortByPrefixLength` - it receives in input an array of prefixes and returns an array sorted by the amount of bits of the netmask (from less specific to more specific)

* `expandIP` - if you provide something like "127/8", you will receive "127.0.0.0/8". If you provide "2001:db8:123::", you will receive "2001:db8:123:0:0:0:0:0"

* `isEqualIP` - it checks for IP equality, it takes into account expansions and cases. E.g. "2001:db8:123::" is equal to "2001:DB8:123::0"

* `isEqualPrefix` - same as above, but with prefixes

* `getAddressFamily` - it returns 4 or 6 (integers)

* `toBinary` - it returns the binary representation of the IP

* `applyNetmask` - it applies the netmask. E.g., if you provide "99.88.77.0/24" you will get the binary representation of "99.88.77.0" truncated at 24 bits

* `isSubnet` - you provide two prefixes and you will get true if the second one is subnet of the first one.

* `isSubnetBinary` - same as above but directly with binary representation