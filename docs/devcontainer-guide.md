# Devcontainer 변경 후 Codespaces 적용 방법 가이드

## 개요

devcontainer 설정을 통해 Codespaces 환경을 자동으로 구성할 수 있습니다.  
하지만 이미 생성된 Codespaces 환경에서는 devcontainer 설정이 변경되어도 자동으로 반영되지 않습니다.

이 문서는 변경된 devcontainer 설정을 기존 Codespaces 환경에 적용하는 방법을 설명합니다.

---

## 왜 자동으로 적용되지 않을까?

Codespaces는 생성 시점의 devcontainer 설정을 기반으로 컨테이너를 구성합니다.

따라서 이후에 `.devcontainer/devcontainer.json` 파일이 변경되더라도  
기존 Codespace에는 자동으로 적용되지 않습니다.

---

## 적용 방법

### 방법 1: Rebuild Container (권장)

1. Codespaces 실행  
2. `Ctrl + Shift + P`  
3. `Codespaces: Rebuild Container` 실행  

→ 최신 devcontainer 설정 적용됨

---

### 방법 2: Codespace 재생성

1. 기존 Codespace 삭제  
2. 새 Codespace 생성  

단점: 기존 작업 사라질 수 있음

---

## Rebuild vs 재생성

| 항목 | Rebuild | 재생성 |
|------|--------|--------|
| 기존 작업 유지 | O | X |
| 설정 적용 | O | O |

---

## 정리

- devcontainer 변경 후 기존 Codespace에는 자동 반영되지 않음  
- Rebuild Container로 쉽게 적용 가능  
- 재생성은 마지막 방법
