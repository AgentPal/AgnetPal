# Pal Contacts

## Purpose

This document explains how AgentPal discovers registered Pals.

## Current Status

Short placeholder for v0.3.0-rc.1 and the v0.4 local structure foundation.

## Source Of Truth

`workspace/organization/contacts/` is the source of truth for Pal discovery. Old root `contacts/` records were archived under `archive/migration-from-v0.3/root-legacy/contacts/`; legacy registry records now live under `workspace/resources/registry/` and are compatibility references only.

Only valid Pal Packs should become contacts. Skills, tools, models, plugins, MCP servers, raw repositories, runtime adapters, knowledge packs, and persona packs are not Pal contacts.

## To Add Later

- Contacts file examples.
- Registry refresh process.
- Unknown Pal handling.

## Related

- [Contacts and registry](../03-pal-pack-standard/10-contacts-and-registry.md)
- [Official Pals](../99-reference/official-pals.md)
