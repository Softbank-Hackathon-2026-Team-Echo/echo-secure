# echo-secure
보안·거버넌스 — 보안 결과 수집·공통 정책·매트릭스 (임시 생성; 실제 구현 위치는 파트 논의)

## 보안 SPEC·코드 위치 안내

이 저장소에는 지금 이 README만 있습니다. 보안·거버넌스 작업은 아래 저장소에 있습니다.

- **보안·거버넌스 SPEC**: echo-was [`specs/sec-*.md`](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/tree/main/specs)
  - [sec-1 보안 통제·증거 출처·검사 시점](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/specs/sec-1-security-controls.md)
  - [sec-2 검사 원문 정규화 + TLS 접속 시험](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/specs/sec-2-finding-normalizers.md) · [sec-2-2 findings 표](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/specs/sec-2-2-findings-table.md) · [sec-2-3 빌드 보안 검사 원문 → findings](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/specs/sec-2-3-build-scan-collect.md)
  - [sec-3 공통 보안 규칙표·이전 허용 판정](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/specs/sec-3-rule-table.md) · [sec-3-2 기한부 예외 API](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/specs/sec-3-2-security-exceptions-api.md)
  - [sec-4 보안 매트릭스·증거 조회 API](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/specs/sec-4-security-matrix-api.md)
  - [sec-5 이전 승인·실행 시작 보안 게이트](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/specs/sec-5-migration-gate.md)
  - [sec-11 고객 빌드 이미지·소스 보안 검사](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/specs/sec-11-build-scan.md)
  - [sec-ai 기한부 예외 + AI 실행 표 스키마](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/specs/sec-ai-base-schema.md)
- **코드**: echo-was [`app/services/security_gate.py`](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/app/services/security_gate.py) · [`app/routers/security_router.py`](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/app/routers/security_router.py) · [`app/routers/security_exception_router.py`](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/app/routers/security_exception_router.py)
- **고객 앱 보안 검사 워크플로**(빌드 뒤 Trivy·gitleaks, 결과 `security-scan`): echo-was [`.github/workflows/customer-build.yml`](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-was/blob/main/.github/workflows/customer-build.yml) — echo-infra에는 워크플로 파일이 없습니다(11/5 `git/trees/main` 기준)
- **인프라 쪽 보안 SPEC**: echo-infra [`specs/wif-build-main-only.md`](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-infra/blob/main/specs/wif-build-main-only.md)(빌드 신원 main 전용) · [`specs/ai-sandbox-network.md`](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-infra/blob/main/specs/ai-sandbox-network.md)(AI 샌드박스 망) · [CVE-2026-98432 대응 기록](https://github.com/Softbank-Hackathon-2026-Team-Echo/echo-infra/blob/main/docs/team/security/cve-2026-98432-response.md)

작성: 김지민 (11/5)
