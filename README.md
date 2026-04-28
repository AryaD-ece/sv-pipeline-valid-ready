# SystemVerilog Valid-Ready Pipeline (1-Stage)

## Overview
This project implements and verifies a 1-stage valid-ready pipeline using SystemVerilog.

The design models a backpressure-aware data path where:
- Producer drives `valid`
- Consumer drives `ready`
- Data transfer occurs only when both are asserted

## Features
- Single-stage pipeline with flow control
- Supports backpressure (consumer stalls)
- Handles back-to-back transactions
- Transaction counter for verification

## Verification Strategy
A constrained-random testbench is used:
- Randomized data and inter-transaction delays
- Random consumer backpressure
- Mailbox-based scoreboard
- Cycle-accurate checking

## Simulation Results
- Total transactions: 20
- PASS: 20
- FAIL: 0
- Functional correctness verified

## Project Structure

src/
pipeline_dut.sv

sim/
tb_pipeline.sv
transaction.sv


## How to Run
1. Open in Vivado Simulator
2. Run behavioral simulation
3. Observe waveform and console output

## Key Concepts Demonstrated
- Valid-ready handshake protocol
- Flow control and backpressure
- Constrained random verification
- Mailbox communication
- Scoreboarding

## Author
Arya Dinesh  
ECE Undergraduate
