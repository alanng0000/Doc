# **Sema Sema Memory**


Sema Sema Memory stores permanently Sema Prom.


Sema Sema Memory also stores data persistently.
This store is addressable.
Data is readed from it and writed to it with compute op.

Addressable store has 2^64 addresses.
Address starts from 0. Address increments 1 for each next address. The last address is 2^64 - 1.
Address refers to one byte in the addressable store.
The first byte is at address 0.
For any byte A that is not the byte at last address, the next byte is at address that is address of A added with 1.
The byte at last address has no next byte because there is no next address.