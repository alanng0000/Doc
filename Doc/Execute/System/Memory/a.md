# **Execute System Memory**


Execute System Memory stores permanently Execute Program.


Execute System Memory also stores data persistently.
This store is addressable.
Data is readed from it and writed to it with compute commands.

Addressable store has 2^64 addresses.
Address starts from 0. Address increments 1 for each next address. The last address is 2^64 - 1.
Address refers to one byte in the addressable store.
The first byte is at address 0.
For any byte A, the next byte is at address that is address of A added with 1.