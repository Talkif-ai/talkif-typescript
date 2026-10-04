# Changelog

All notable changes to `@talkif/sdk` are documented here. The SDK is generated from the
public Talkif API definition; see the [API reference](https://docs.talkif.ai) for details.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this
project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html). While the
version is below 1.0.0, a minor release may contain breaking changes; they are listed under
**Removed** or **Changed**.

## [Unreleased]

## [0.3.0] — 2026-10-04

### Added

- Models: `deprecation` on `LlmModel`, `SttModel` and `TtsModel` — a `ModelDeprecation` with
  `retiresOn` and `replacedBy` when a model is scheduled for retirement. Until that date the
  model works as before; from that date calls on it run on the named replacement from the same
  provider. See [When a model is retired](https://docs.talkif.ai/build/choose-models-and-voices#when-a-model-is-retired).

## [0.2.0] — 2026-10-02

### Added

- `transfers`: transfer destinations and destination groups (`createDestination`, `listDestinations`, …, `createGroup`, `listGroups`, …), testing an
  app destination and rotating its signing secret, its delivery log, accepting or declining
  transfer offers (`acceptOffer`, `declineOffer`, `getOffer`), and member tags, available hours and availability
  (`listMembers`, `setMemberTags`, `setMemberHours`, `setMemberAvailability`, …).
- `accounts`: `getRoles()` and `getPermissions()`.
- `calls`: `calls.listCalls()` — one paginated list of calls, filterable by status.
- `public_calls`: `publicCalls.createCall()`, `getCallStatus()`, `relayOffer()` and `endCall()` use the documented `/public/calls` paths.

### Removed

- `calls`: `calls.getActiveCalls()` and `calls.getCallHistory()` are replaced by `calls.listCalls()`. The endpoints still answer, so 0.1.x keeps
  working, but they are no longer part of the SDK.

## [0.1.1] — 2026-09-12

### Changed

- List methods for billing, calls and voice agents take `limit`/`offset` and return typed
  list responses.

### Fixed

- Auto-pagination starts at the first item instead of skipping it.

## [0.1.0] — 2026-09-12

### Added

- First release: calls, public (embedded) calls, voice agents and their functions and
  templates, phone numbers and providers, contacts, do-not-call, campaigns, schedules,
  billing, analytics, models and error codes.

[Unreleased]: https://github.com/Talkif-ai/talkif-typescript/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/Talkif-ai/talkif-typescript/compare/v0.1.1...v0.2.0
[0.1.1]: https://github.com/Talkif-ai/talkif-typescript/compare/v0.1.0...v0.1.1
[0.1.0]: https://github.com/Talkif-ai/talkif-typescript/releases/tag/v0.1.0
