# Context Access List Required Fields Self-Test

## Goal

Verify that Context Access List templates include the required R32 fields.

## Good Behavior

The template includes `recipient_id`, `task`, `can_read_paths`, `can_read_summaries`, `can_receive_outputs_from`, `cannot_read`, `need_output`, `output_contract`, `verification_required`, `content_read_budget`, `index_known_paths`, and `content_read_files`.

## Bad Behavior

The access list only says "read relevant files" or omits content-read tracking.

## Pass / Fail

Pass if required fields exist in protocol, template, and example.

## v0.1 Boundary

The list is a protocol/template, not an enforced sandbox.

