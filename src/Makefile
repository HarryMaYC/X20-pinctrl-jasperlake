# SPDX-License-Identifier: GPL-2.0
# Intel jasperlake pin control drivers

obj-m += pinctrl-jasperlake.o

ifeq (,$(KVER))
  KVER=$(shell uname -r)
endif

#KSRC := /usr/src/linux-headers-$(KVER)
KSRC := /lib/modules/$(KVER)/build

EXTRA_CFLAGS += $(CFLAGS_EXTRA)

all:
	make -C $(KSRC) M=$(PWD) modules

clean:
	make -C $(KSRC) M=$(PWD) clean

