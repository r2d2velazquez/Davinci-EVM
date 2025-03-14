# Makefile for IPIPE applications
CMEMLIB=cmem.a470uC
CC = $(CROSS_COMPILE)gcc -I$(KERNEL_DIR)/include
INSTALL_DIR=$(FINAL_DEST)/imp-prev-rsz

all:	capture_prev_rsz_onthe_fly_yuv \
	capture_prev_rsz_onthe_fly_bayer \
	capture_prev_rsz_ss_raw_yuv\
	do_preview_resize \
	do_resize_420_420 \
	do_resize \
	display

capture_prev_rsz_onthe_fly_yuv: capture_prev_rsz_onthe_fly_yuv.o
	$(CC) -o  capture_prev_rsz_onthe_fly_yuv $^ $(CMEMLIB)

capture_prev_rsz_onthe_fly_bayer: capture_prev_rsz_onthe_fly_bayer.o
	$(CC) -o  capture_prev_rsz_onthe_fly_bayer $^ $(CMEMLIB)

capture_prev_rsz_ss_raw_yuv: capture_prev_rsz_ss_raw_yuv.o
	$(CC) -o  capture_prev_rsz_ss_raw_yuv $^ $(CMEMLIB)

do_preview_resize: do_preview_resize.o
	$(CC) -o  do_preview_resize $^ $(CMEMLIB)

do_resize_420_420: do_resize_420_420.o
	$(CC) -o  do_resize_420_420 $^ $(CMEMLIB)

do_resize: do_resize.o
	$(CC) -o  do_resize $^ $(CMEMLIB)

display: display.o
	$(CC) -o  display $^ $(CMEMLIB)

install:
	mkdir -p 				$(INSTALL_DIR)
	cp capture_prev_rsz_onthe_fly_yuv	$(INSTALL_DIR)
	cp capture_prev_rsz_onthe_fly_bayer	$(INSTALL_DIR)
	cp capture_prev_rsz_ss_raw_yuv		$(INSTALL_DIR)
	cp do_preview_resize			$(INSTALL_DIR)
	cp do_resize_420_420			$(INSTALL_DIR)
	cp do_resize				$(INSTALL_DIR)
	cp display				$(INSTALL_DIR)

clean:
	rm -f *.o *~
	rm -f capture_prev_rsz_onthe_fly_bayer \
	capture_prev_rsz_onthe_fly_yuv \
	capture_prev_rsz_ss_raw_yuv\
	do_preview_resize \
	do_resize_420_420 \
	do_resize \
	display
