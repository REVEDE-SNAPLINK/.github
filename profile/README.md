# Snaplink

**Snaplink**는 고객과 스냅 작가를 연결하는 C2C 스냅 촬영 중개 플랫폼입니다.  
사용자는 촬영 목적과 분위기에 맞는 작가를 탐색하고, 작가의 포트폴리오와 프로필을 확인한 뒤 문의·예약 흐름으로 이어질 수 있습니다.

Revede 팀은 모바일 앱, 랜딩페이지, 관리자 페이지, 데이터 계측 환경을 함께 구축하며 초기 MVP를 출시하고 운영 검증을 진행했습니다.

## Service Overview

Snaplink는 스냅 촬영 과정에서 발생하는 탐색과 연결 문제를 해결하는 것을 목표로 합니다.

- 고객은 원하는 촬영 카테고리와 작가를 탐색할 수 있습니다.
- 작가는 포트폴리오와 프로필을 통해 자신의 작업을 보여줄 수 있습니다.
- 문의와 예약 흐름을 통해 고객과 작가가 연결될 수 있습니다.
- 운영자는 관리자 페이지에서 사용자, 작가, 예약, 문의, CS, 마케팅 데이터를 확인할 수 있습니다.

## Main Features

### Mobile App

- 카테고리 기반 스냅 촬영 탐색
- 작가 검색 및 프로필 조회
- 작가 포트폴리오 확인
- 문의·예약 플로우
- 후기 작성 플로우
- 회원가입·로그인 및 사용자 상태 관리
- Airbridge 기반 유입 및 딥링크 처리

### Landing Page

- 서비스 소개
- 작가/고객 대상 주요 가치 설명
- FAQ, 공지, 문의 동선 제공
- 앱 다운로드 및 Airbridge 기반 유입 연결

### Admin Console

- 사용자 및 작가 관리
- 문의·예약·후기 등 운영 데이터 확인
- CS 및 운영 대응을 위한 내부 관리 화면
- Firebase Analytics, Airbridge, BigQuery 기반 사용자 행동·유입 데이터 확인 구조

## Architecture

```txt
User / Customer
      │
      ▼
React Native Mobile App
      │
      ├── Authentication / User State
      ├── Artist Search / Profile / Portfolio
      ├── Inquiry / Reservation Flow
      └── Analytics Events
              │
              ├── Firebase Analytics
              ├── Airbridge
              └── BigQuery

Landing Page ───────► App Download / Airbridge Attribution

Admin Console ──────► Operation, CS, Marketing, KPI Monitoring
```

## Tech Stack

### App / Web

- React Native
- React
- TypeScript / JavaScript
- React Query
- Zustand

### Data & Operation

- Firebase Analytics
- Airbridge
- BigQuery
- Deep Link / Attribution Tracking

### Deployment / Platform

- iOS App Store
- Google Play Store
- Web hosting for landing and admin pages

## Current Status

- 2026년 2월 iOS·Android 앱 출시
- 초기 사용자 약 120명 가입
- 본격적인 마케팅과 PMF 검증은 진행 전 단계
- 초기 MVP 출시와 사용자 행동 데이터 수집 환경 구축 완료

## Links

- Website: https://www.snaplink.run
- GitHub Organization: https://github.com/REVEDE-SNAPLINK
