# Crypt_hw_serial
Software Serial Protection for Raspberry Pi

(This lib is to be used with SERIAL ST2W16)

Step-by-step:
1)	Switch off your Raspberry Pi;
2)	Attach device to GPIO according with image (device uses the GPIO Pins from 17 to 26);
3)	Power on your Raspberry Pi;
4)	Use set_key application to set up your private key;
    e.g.  set_key  A3768BF214E4CC897D901AA22FF69A34
5)	Change the key_array, of file serial_check.h, according with previous key;
6)	Function  serial_number_check_procedure will check if stored serial match with input parameter sys_serial;
7)	Compile your application linking with libCrypt_hw_serial.a
    e.g. gcc test.c -o test -L. -lCrypt_hw_serial

