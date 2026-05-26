# proto — DinoInsure

Protobuf definitions for all DinoInsure services. Generated Java and Python stubs included.

## Structure

```
proto/
├── buf.yaml
├── buf.gen.yaml
└── proto/
    └── dinoinsure/
        ├── common/v1/types.proto        — Money, Language, PolicyType
        ├── auth/v1/auth.proto           — AuthServiceGrpc
        ├── document/v1/document.proto   — DocumentServiceGrpc
        ├── policy/v1/policy.proto       — PolicyServiceGrpc
        ├── chat/v1/chat.proto           — ChatServiceGrpc (server streaming)
        └── notification/v1/            — Kafka event schemas (no gRPC service)
```

## Generate stubs

```bash
buf generate
```

Outputs:
- `generated/java/` — Java stubs for Spring Boot services
- `generated/python/` — Python stubs for FastAPI services

## Lint

```bash
buf lint
```

## Submodule usage

This repo is submoduled into each service at `src/main/proto` (Java) or `proto/` (Python).

```bash
git submodule add https://github.com/dino-wallet/proto src/main/proto
```
