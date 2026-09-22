# Project Requirements — Hybrid Asset & Desk Reservation System

## Problem Statement
Organizations with hybrid work need a way to allocate hot-desks, track loaned hardware (monitors, dongles), and ensure equipment is sanitized/returned between uses.

## User Roles
- Employee: can create/view/edit only their own reservations
- Facilities Manager: full access to all desk reservations
- IT Asset Owner: full access to loaner hardware records only

## Core Entities (draft)
- Desk Reservation
- Loaner Hardware

## Conflict Rule (draft)
- A desk cannot be double-booked for overlapping time windows
- A user cannot hold two active reservations at overlapping times
