CWD=$(shell pwd)
COCOTB_REDUCED_LOG_FMT = True
SIM ?= icarus
# VHDL_SOURCES =$(CWD)/../tinyalu_hdl/vhdl/single_cycle_add_and_xor.vhd \
              $(CWD)/../tinyalu_hdl/vhdl/three_cycle_mult.vhd \
              $(CWD)/../tinyalu_hdl/vhdl/tinyalu.vhd
VERILOG_SOURCES =$(CWD)/tinyalu_hdl/verilog/tinyalu.sv
MODULE := testbench
TOPLEVEL := tinyalu
TOPLEVEL_LANG := verilog
COCOTB_HDL_TIMEUNIT=1us
COCOTB_HDL_TIMEPRECISION=1us
include $(shell cocotb-config --makefiles)/Makefile.sim

cleanall: clean
	@rm -rf __pycache__
	@rm -f results.xml
	@rm -f modelsim.ini
	@rm -f transcript