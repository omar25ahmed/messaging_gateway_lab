# Messaging Gateway Lab

A small Rails application for practicing backend design and testing around provider-backed messaging workflows.

The app models a simplified omnichannel messaging gateway: accounts connect external channels, messages move through provider boundaries, and incoming provider events need to be handled safely. The focus is not to build a production messaging platform, but to work through realistic Rails/RSpec problems that appear in provider-heavy applications.

## Current Focus

This repo is intentionally being built in small slices:

- domain modeling for accounts, channel connections, contacts, messages, and provider events
- RSpec coverage that protects behavior instead of framework defaults
- factories that make test setup readable without hiding important state
- request specs for JSON/API flows
- provider-boundary tests using fakes, stubs, or WebMock where appropriate
- failure cases such as duplicate webhooks, invalid payloads, provider errors, and out-of-order events

## Tech Stack

- Ruby on Rails
- RSpec
- FactoryBot
- WebMock
- SQLite for local development and test speed

## Why This Exists

This is a hands-on Rails/RSpec lab for improving testing judgment in backend systems. The goal is to make testing decisions explicit: what deserves coverage, which level of test gives the right confidence, where mocks help, where they hide risk, and how specs can support future refactoring.

## Status

Early-stage Rails app. The initial work is focused on the domain model and test setup before adding API and provider integration behavior.
