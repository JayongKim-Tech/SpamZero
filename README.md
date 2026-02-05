# 🛡️ SpamZero (iOS)
**"070 패턴 스팸, 비트 단위의 정밀함으로 완벽하게 제어합니다."**

[![Platform](https://img.shields.io/badge/Platform-iOS-lightgrey?style=flat-square&logo=apple)]()
[![Framework](https://img.shields.io/badge/Framework-.NET%20MAUI-blueviolet?style=flat-square)]()
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)]()

## 🚀 프로젝트 개요 (Overview)
`SpamZero`는 단순한 번호 DB 기반의 차단을 넘어, **패턴(Prefix) 매칭**을 통해 지능적으로 변하는 070 스팸 전화에 대응하는 초경량 iOS 차단 엔진입니다. .NET MAUI를 기반으로 하며, 애플의 기술적 제약을 **Bitset 알고리즘**으로 극복하여 압도적인 메모리 효율성을 자랑합니다.

## ✨ 핵심 기능 (Key Features)
- **무조건적 패턴 차단**: 070, 080 등 특정 접두사로 시작하는 모든 번호를 DB 업데이트 없이 즉각 차단합니다.
- **초경량 최적화 엔진**: 1억 개의 번호를 단 12.5MB의 비트셋으로 매핑하여 메모리 사용량을 극한으로 절감했습니다.
- **스트리밍 데이터 전송**: iOS CallKit Extension의 20MB RAM 제한을 우회하는 `yield return` 방식의 스트리밍 제출 로직을 탑재했습니다.
- **전문가급 미니멀 UI**: 복잡한 설정 없이 마스터 스위치 하나로 모든 기능을 제어하는 하이엔드 다크 모드 UI를 제공합니다.

## 🛠️ 기술 스택 (Tech Stack)
- **Language**: C# (.NET 8)
- **Framework**: .NET MAUI
- **Native API**: CallKit (Call Directory Extension)
- **Data Structure**: Optimized BitArray (Custom Bitset Mapping)

## 📐 핵심 로직 (Core Logic)
### 1. Bitset Mapping
전화번호의 존재 여부를 1비트(0 or 1)로 관리하여 메모리 점유율을 800MB에서 12MB 수준으로 **약 98% 압축**했습니다.

### 2. Sorted Streaming
iOS 시스템이 요구하는 오름차순 정렬 조건을 만족하기 위해, 별도의 정렬 연산 없이 비트셋 인덱스를 순차적으로 스캔하여 번호를 생성 및 전송합니다.

## 🎨 UI/UX 철학
- **Simplicity**: 사용자는 오직 'On/Off'와 '차단 대역 추가'만 고민하면 됩니다.
- **Professionalism**: 고대비 블랙 테마와 네온 블루 포인트를 사용하여 시스템 엔진으로서의 신뢰감을 줍니다.

## 📅 로드맵 (Roadmap)
- [ ] Bitset 추출 엔진(ExtractNumbers) 고도화
- [ ] iOS CallKit Extension 연동 및 테스트
- [ ] 월 990원 인앱 결제(In-App Purchase) 구현
- [ ] 사용자 정의 접두사(Prefix) 관리 기능 완성

## 📄 라이선스 (License)
본 프로젝트는 MIT 라이선스를 따릅니다.
