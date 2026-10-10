# TaskFlow · Offline-first Task Manager

A React Native task manager with persistent local data, scheduled reminders, map locations and a synchronization queue.

**Stack:** React Native · Expo · TypeScript · Zustand · AsyncStorage · React Native Paper

## Features

- Task creation, editing, status transitions and activity history.
- Image/document attachment metadata and local file persistence.
- Local notifications and task locations on a map.
- Offline changes with Last-Write-Wins synchronization to a mock REST server.

## Local setup

Node.js and npm; an Expo-compatible simulator/device. The mock backend uses json-server.

```bash
npm ci
cp .env.example .env
npm run server
# In another terminal:
npm start
```

## Validation commands

```bash
npm run verify
```

These are reproducible commands, not a claim that the full application suite passed during portfolio preparation. See the workspace validation report for checks actually run.

## Structure

```text
src/screens/    task and settings screens
src/services/   persistence, sync, reminders and attachment services
src/store/      state stores
src/utils/      validation and helpers
scripts/        mock backend launcher and seed data
```

## Limitations and configuration

This originated as a React Native internship technical assignment. The mock backend has no production authentication, attachment binaries are not synchronized and clock-based conflict resolution has trade-offs. The original assignment context and AI tooling disclosure are retained in docs/ORIGINAL_README.md. Runtime db.json and generated native output are excluded.

## Further documentation

[Original project documentation](docs/ORIGINAL_README.md) is preserved for implementation details and original context.
