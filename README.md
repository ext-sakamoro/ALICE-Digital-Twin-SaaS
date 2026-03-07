# ALICE-Digital-Twin

Physics-accurate digital twin platform with SDF geometry and real-time rendering

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum |

## ALICE Crate Integration

alice-physics, alice-sdf, alice-kinematics, alice-view

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/v1/simulate` | 物理シミュレーション実行 |
| `POST` | `/api/v1/scene` | SDF シーン構築 |
| `POST` | `/api/v1/motion` | キネマティクス軌道計算 |
| `GET ` | `/api/v1/render` | リアルタイムレンダリング |
| `GET ` | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
