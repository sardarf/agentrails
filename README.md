# ProvingGround

ProvingGround is safety and testing infrastructure for autonomous and semi-autonomous DeFi agents on Arbitrum.

As AI agents begin to interact with onchain protocols, execution is becoming easier, but safety remains the real bottleneck. Builders need to know whether an agent strategy is profitable, resilient, and risk-aware before allowing it to move real funds.

ProvingGround helps solve this by turning strategy testing into enforceable onchain policy.

## Core Idea

A developer defines a DeFi agent strategy, configures risk limits, runs a backtest, and generates an Agent Execution Policy.

That policy is then enforced by a Solidity `PolicyGuard` contract. If the agent tries to execute an action outside the approved limits, the contract rejects it automatically.

Safety is not only shown in a report. It is enforced onchain.

## What It Does

ProvingGround allows builders to:

- Define an agent strategy
- Configure risk limits
- Simulate strategy behavior
- Review P&L, drawdown, exposure, and failed conditions
- Generate an Agent Execution Policy
- Enforce the policy through a smart contract
- Demonstrate valid and invalid agent actions onchain

## Example Policy Rules

A policy may define rules such as:

- Maximum exposure per strategy
- Minimum APY threshold
- Maximum drawdown
- Maximum transaction size
- Rebalance frequency
- Human approval threshold
- Approved protocols or strategies

If an agent action breaks these limits, `PolicyGuard` rejects it.

## MVP Scope

The buildathon MVP focuses on stablecoin and yield strategies on Arbitrum, such as:

- USDC lending strategy
- Stablecoin yield strategy
- Simple treasury rebalancing strategy

The MVP will include:

- Strategy configuration screen
- Simple backtesting engine
- Risk report
- Agent Execution Policy JSON
- Solidity `PolicyGuard` contract
- Demo agent execution flow
- Onchain accepted/rejected action demo

## Demo Goal

The key demo will show:

1. A developer defining a DeFi agent strategy.
2. The system running a simple backtest.
3. ProvingGround generating an Agent Execution Policy.
4. The policy being stored in the `PolicyGuard` contract.
5. A valid agent action being accepted.
6. An out-of-bounds agent action being rejected onchain.

This demonstrates the main principle of ProvingGround:

> Safety is enforced by the contract, not promised by the backtest.

## Why Arbitrum

Arbitrum is a strong environment for DeFi, stablecoin liquidity, and agentic applications. ProvingGround is designed to support safer agentic DeFi by giving builders a way to test, constrain, and audit autonomous strategies before real capital is exposed.

## Status

This project is currently in early buildathon development for the Arbitrum Open House London Buildathon.
