CWD=$(shell pwd)
COCOTB_REDUCED_LOG_FMT = True
SIM ?= icarus
VERILOG_SOURCES =$(CWD)/clocker.sv
MODULE := testbench
TOPLEVEL := clocker
TOPLEVEL_LANG := verilog
COCOTB_HDL_TIMEUNIT=1us
COCOTB_HDL_TIMEPRECISION=1us
include $(shell cocotb-config --makefiles)/Makefile.sim

cleanall: clean
	@rm -rf __pycache__
	@rm -f results.xml
	@rm -f modelsim.ini
	@rm -f transcript
