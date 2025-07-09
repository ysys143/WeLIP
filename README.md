# WeLIP (Wedatalab LLM Infrastructure Platform)

WeLIP은 대규모 언어 모델(LLM) 기반 AI 인프라 플랫폼으로, 확장 가능하고 안정적인 AI 서비스를 제공하기 위한 종합 솔루션입니다.

## 🎯 프로젝트 목표

- **확장 가능한 AI 인프라**: GPU 분산 처리를 통한 고성능 AI 서비스 제공
- **표준화된 아키텍처**: 모듈화된 레이어드 아키텍처로 유지보수성 확보
- **운영 효율성**: 자동화된 배포, 모니터링, 스케일링 시스템 구축
- **비용 최적화**: 리소스 효율적인 운영을 통한 비용 절감

## 🏗️ 시스템 아키텍처

### 레이어드 아키텍처
```
┌─────────────────────────────────────────┐
│           API Gateway Layer            │  ← FastAPI, 인증, 라우팅
├─────────────────────────────────────────┤
│        Application Layer               │  ← 비즈니스 로직, 에이전트 체인
├─────────────────────────────────────────┤
│          Service Layer                 │  ← ML 모델 서빙, 분산 처리
├─────────────────────────────────────────┤
│           Data Layer                   │  ← 벡터 DB, 캐시, 스토리지
├─────────────────────────────────────────┤
│       Infrastructure Layer             │  ← Kubernetes, 모니터링
└─────────────────────────────────────────┘
```

## 📈 구현 로드맵

### Phase 1: 극단적 MVP (7월)
- ✅ 기본 FastAPI 서버 구축
- 🔄 로컬 모델 서빙
- ⏳ 간단한 에이전트 체인
- ⏳ 기본 모니터링

### Phase 2: 안정화 및 확장 (8월~9월)
- 아키텍처 리팩토링
- GPU 분산 처리 도입 (Ray)
- 고급 에이전트 기능
- 종합 모니터링 시스템

### Phase 3: 운영 고도화 (9월~10월)
- Kubernetes 배포
- Ray 클러스터 통합
- 고급 실험 관리
- 보안 강화 및 CI/CD

## 🛠️ 기술 스택

### 백엔드
- **Web Framework**: FastAPI
- **분산 처리**: Ray, Python multiprocessing
- **ML 프레임워크**: PyTorch, Transformers
- **데이터베이스**: Qdrant (벡터), Redis (캐시)

### 인프라
- **컨테이너화**: Docker
- **오케스트레이션**: Kubernetes
- **모니터링**: Prometheus + Grafana
- **실험 추적**: MLflow

### 개발 도구
- **패키지 관리**: uv
- **버전 관리**: Git + GitHub
- **CI/CD**: GitHub Actions
- **문서화**: MkDocs + Mermaid

## 📁 프로젝트 구조

```
WeLIP/
├── docs/                           # 문서 및 다이어그램
│   ├── chart/                      # 아키텍처 다이어그램 (PNG)
│   └── plan/                       # 계획 문서 (Markdown)
├── src/                           # 소스 코드 (예정)
├── tests/                         # 테스트 코드 (예정)
├── infra/                         # 인프라 설정 (예정)
└── README.md                      # 프로젝트 소개
```

## 📊 아키텍처 다이어그램

프로젝트의 주요 아키텍처 다이어그램들:

- [레이어드 아키텍처](docs/chart/WeLIP_레이어드_아키텍처.png)
- [점진적 확장 전략](docs/chart/WeLIP_점진적_확장_전략.png)
- [요청 처리 흐름](docs/chart/WeLIP_요청_처리_흐름.png)
- [ML 파이프라인](docs/chart/WeLIP_ML_파이프라인.png)
- [GPU 분산 처리](docs/chart/WeLIP_GPU_분산_처리_및_표준성_진화.png)
- [구현 로드맵](docs/chart/WeLIP_구현_계획_로드맵_2025년7월.png)

## 📋 시작하기

### 요구사항
- Python 3.11+
- uv (패키지 관리)
- Docker (컨테이너화)
- Git

### 개발 환경 설정
```bash
# 프로젝트 클론
git clone https://github.com/YOUR_USERNAME/WeLIP.git
cd WeLIP

# Python 환경 설정 (uv 사용)
uv venv
source .venv/bin/activate  # macOS/Linux
# .venv\Scripts\activate   # Windows

# 의존성 설치 (향후 추가 예정)
# uv pip install -r requirements.txt
```

## 🤝 기여하기

WeLIP은 오픈소스 프로젝트입니다. 기여를 환영합니다!

1. Fork 후 개발 브랜치 생성
2. 코드 변경 및 테스트
3. Pull Request 제출

## 📝 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다.

## 📞 연락처

문의사항이나 제안사항이 있으시면 Issues를 통해 연락주세요.

---

**WeLIP** - AI의 미래를 함께 만들어가는 인프라 플랫폼 