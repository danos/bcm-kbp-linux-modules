#
#  Copyright 2015-2019 Broadcom. All rights reserved.
#  The term "Broadcom" refers to Broadcom Inc. and/or its subsidiaries.
#  
#  This program is free software; you can redistribute it and/or modify
#  it under the terms of the GNU General Public License, version 2, as
#  published by the Free Software Foundation (the "GPL").
#  
#  This program is distributed in the hope that it will be useful, but
#  WITHOUT ANY WARRANTY; without even the implied warranty of
#  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
#  General Public License version 2 (GPLv2) for more details.
#  
#  You should have received a copy of the GNU General Public License version 2 (GPLv2)
#  along with this program; if not, write to the Free Software
#  Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.
#

obj-m := kbp_driver.o

KERNELDIR := /lib/modules/$(shell uname -r)/build

##     useful option for building modules:
##     make KBUILD_VERBOSE=1
##     make V=1

PWD := $(shell pwd)

default:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules

clean:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) clean
	rm -rf *.o *.ko *.mod.c *.mod.o .*.cmd .tmp_versions Module.symvers *~
