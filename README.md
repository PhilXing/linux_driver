# linux_driver

* install toolchain & headers of current kernel before make:

        sudo apt install -y build-essential linux-headers-$(uname -r)
        
* make && install/remove/check this driver module

        make
        sudo insmod ./example.ko
        sudo mknod /dev/example c 60 0
        sudo chmod 666 /dev/example
        echo -n 'abcd' > /dev/example
        sudo rmmod example
        sudo dmesg | tail
