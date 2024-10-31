# ASSUME Framework Examples

This repository contains example implementations and usage patterns for the [ASSUME (Agent-Based Electricity Markets Simulation Toolbox)](https://github.com/assume-framework/assume).

## Overview

The ASSUME framework provides automated security measurement and evaluation capabilities for software systems. These examples demonstrate how to integrate and utilize ASSUME in various scenarios.

## Getting Started

1. Clone this repository

`git clone https://github.com/assume-framework/assume-examples.git`


2. Install assume framework

In your selected python environment (virtualenv or conda) run:

`pip install assume-framework`

3. Run the examples

If you want to have a database running and the grafana available run: `docker compose up -d` (make sure you have docker installed).

Then run the tiny example:

`assume -i inputs -s example_01a -c tiny -db "postgresql+psycopg2://assume:assume@localhost:5432/assume"`

or more general:

`assume -i inputs -s $scenario_name -c $case_study -db $database_url`

## Examples

The available examples are as follows:

### example_01 contains a small sample scenario

#### example_01a
* base: simple small example
* dam: small_dam
* dam_with_complex_clearing: small_with_opt_clearing

#### example_01b
* base: small_with_vre

#### example_01c
* eom_only: small_with_vre_and_storage
* dam_with_complex_opt_clearing: small_with_BB_and_LB
* dam_with_complex_opt_clearing: small_with_vre_and_storage_and_complex_clearing
* eom_and_crm: small_with_crm

#### example_01d
* base: small_with_redispatch
* nodal_case: small_with_nodal_clearing
* zonal_case: small_with_zonal_clearing

#### example_01f
* eom_case: market_study_eom
* ltm_case: market_study_eom_and_ltm

### example_02 contains learning examples

#### example_02a
* base: small_learning_1
* base_lstm: small_learning_1_lstm

#### example_02b
* base: small_learning_2
* base_lstm: small_learning_2_lstm

#### example_02c
* base: small_learning_3

#### example_02d
* dam: learning_with_complex_bids

#### example_03
* base_case_2019: large_2019_eom
* eom_crm_case_2019: large_2019_eom_crm
* dam_case_2019: large_2019_day_ahead
* base_case_2019_with_DSM: large_2019_with_DSM

### examples_03 contains a large 2019 examples of germany

#### example_03a
* base_case_2019: large_2019_rl

#### example_03b
* base_case_2021: large_2021_rl

### example_05 contains an updated redispatch example of germany

#### example_05a
* base: redisp_valid_2_nodes

#### example_05b
* base: redisp_valid_3_nodes

#### example_05c
* base: redisp_valid_Germany_2019

#### example_05d
* base: redisp_valid_Germany_2023

## Contributing

Contributions are welcome! If you want to add your example, make sure it works and create a PR for it.

## License

This project contains examples which are licensed as [CC-BY-4.0](https://spdx.org/licenses/CC-BY-4.0.html) if not stated otherwise in the respextive license file.
