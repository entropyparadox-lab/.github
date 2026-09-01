<div align="center">

# ⚡ 엔트로피패러독스 랩 (EntropyParadox Lab)

**초경량 무비용 시스템 엔지니어링, 결정론적 AI 에이전트 인프라 및 순수 Zig v0.16.0+ 프리미티브**

**[ English ](README.md)** • **[ 한국어 ](README.ko.md)** • **[ 日本語 ](README.ja.md)** • **[ 简体中文 ](README.zh.md)**

<p align="center">
  <img src="https://img.shields.io/badge/Language-Zig_v0.16.0+-f7a41d.svg?style=flat-square&logo=zig&logoColor=white" alt="Zig 0.16" />
  <img src="https://img.shields.io/badge/Language-Rust_Edition_2024-000000.svg?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/License-MIT%20%7C%20Apache--2.0-blue.svg?style=flat-square" alt="License" />
  <img src="https://img.shields.io/badge/Architecture-AOT%20%7C%20Zero--Alloc-success.svg?style=flat-square" alt="Zero-Alloc" />
</p>

</div>

---

## 🏛️ 미션 및 엔지니어링 철학

엔트로피패러독스 랩은 고밀도·결정론적 시스템 및 개발자 기반 도구를 개발합니다. 추상화 오버헤드와 비결정론적 런타임 비용을 제거하며 다음 2대 핵심 분야에 집중합니다:

1. **결정론적 AI 에이전트 런타임**: 자율 코딩 에이전트를 위한 마이크로초 단위 실행 하네스, 샌드박스 런타임, 자가 치유 액션 캐시 구축.
2. **순수 Zig (v0.16.0+) 시스템 생태계**: 외부 C 라이브러리 의존성 없는 제로 힙 할당(`0-Alloc`), 컴파일 타임 검증 시스템 프리미티브 개발.

```
┌──────────────────────────────────────────────────────────────────────────┐
│                         엔트로피패러독스 생태계                          │
├────────────────────────────────────┬─────────────────────────────────────┤
│      결정론적 AI 에이전트 인프라   │     순수 Zig (v0.16.0+) 시스템 제품군│
├────────────────────────────────────┼─────────────────────────────────────┤
│ • web-reflex (초고속 액션 캐시)    │ • zig-doc-engine (오프라인 FTS5 검색)│
│ • mos (Firecracker MicroVM PaaS)   │ • zmcp & zmcp-gateway (네이티브 MCP) │
│ • maniac-killer (프로세스 감시자)  │ • zcli, zserde, zenv (코어 유틸)     │
│ • argus-audit (호스트 활동 감사)   │ • zlog, zfetch, zbench (성능/로깅)   │
└────────────────────────────────────┴─────────────────────────────────────┘
```

---

## 🚀 주요 오픈소스 프로젝트

### 1. 🤖 자율 AI 에이전트 인프라

* **[`web-reflex`](https://github.com/entropyparadox-lab/web-reflex)**: AI 웹 에이전트를 위한 결정론적 초고속(<45ms) 자가 치유 액션 캐시. 불필요한 LLM 브라우저 탐색 루프 제거.
* **[`mos`](https://github.com/entropyparadox-lab/mos)**: Linux KVM 및 Firecracker MicroVM 기반의 초경량·고밀도 Scale-to-Zero 서버리스 PaaS.
* **[`maniac-killer`](https://github.com/entropyparadox-lab/maniac-killer)**: 무한 루프나 과점유에 빠진 에이전트 프로세스를 감시하고 강제 격리하는 감시자 엔진.
* **[`argus-audit`](https://github.com/entropyparadox-lab/argus-audit)**: 순수 Rust로 작성된 제로 오버헤드 호스트 활동 및 개발자 감사 엔진.

---

### 2. ⚡ Zig (v0.16.0+) 시스템 제품군

모든 Zig 패키지는 **Zig v0.16.0+** 표준(`std.Io`, `std.process.Init`)을 엄격히 준수하며, 힙 메모리 할당 없는 초경량 설계를 적용했습니다.

* **[`zig-doc-engine`](https://github.com/entropyparadox-lab/zig-doc-engine)**: 550KB 미만의 초경량 오프라인 FTS5 문서 색인/검색 엔진. LLM 컴파일 0-에러 보장.
* **[`zmcp`](https://github.com/entropyparadox-lab/zmcp)** & **[`zmcp-gateway`](https://github.com/entropyparadox-lab/zmcp-gateway)**: 순수 Zig 기반 초고속 Model Context Protocol (MCP) SDK 및 도구 멀티플렉서.
* **[`zcli`](https://github.com/entropyparadox-lab/zcli)**: Zero-Allocation Comptime 선언형 CLI 파서 및 자동 셸 완성기.
* **[`zserde`](https://github.com/entropyparadox-lab/zserde)**: Zero-Allocation 다중 포맷 직렬화 및 Comptime 스키마 유효성 검사 툴킷.
* **[`zenv`](https://github.com/entropyparadox-lab/zenv)**: Zero-Allocation `.env` 파서 및 Comptime 환경변수 주입기.
* **[`zlog`](https://github.com/entropyparadox-lab/zlog)**: ANSI/NDJSON 포맷터 및 OpenTelemetry 추적을 지원하는 무할당 정형 로거.
* **[`zfetch`](https://github.com/entropyparadox-lab/zfetch)**: `std.http.Client` 기반 인체공학적 타입 세이프 HTTP 클라이언트.
* **[`zbench`](https://github.com/entropyparadox-lab/zbench)**: 통계적 마이크로 벤치마킹 및 메모리 프로파일링 도구.
* **[`zig-inspect`](https://github.com/entropyparadox-lab/zig-inspect)**: AI 에이전트 및 개발자를 위한 AST 심볼 인스펙터.

---

### 3. 📖 기술 문서 및 가이드

* **[`zig-guide-kr`](https://github.com/entropyparadox-lab/zig-guide-kr)**: Zig v0.16.0 공식 레퍼런스 완역 및 Rails Guides 스타일의 실전 시스템 프로그래밍 가이드북.

---

## 🛡️ 거버넌스 및 품질 원칙

* **4-Gate 적대적 검증**: 모든 기획, 로드맵, PR은 4단계 사전 적대적 검증(Hate/Falsification)을 거칩니다.
* **태그 불변 원칙**: Semantic Versioning 2.0 및 단방향 전진 릴리스 태그(`vX.Y.Z`) 준수.
* **브랜치 보호**: 로컬 Pre-push 훅 및 GitHub 브랜치 보호를 통해 `main` 직접 푸시 엄격 차단.
* **이중 라이선스**: 모든 오픈소스는 **MIT** 또는 **Apache-2.0** 이중 라이선스로 배포됩니다.

---

<div align="center">
  <sub>Maintained with precision by EntropyParadox Lab.</sub>
</div>
