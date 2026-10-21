# SH Auto Seller · Windows 설치 수정본 v1.0.1

[수정된 프로그램 ZIP 다운로드](downloads/SH_Auto_Seller_Windows_v1_0_1.zip?raw=true)

## pydantic-core / cargo / Visual Studio 설치 오류 수정

기존 실행기는 최신 Python을 선택할 수 있어, 호환 wheel이 없으면 소스 컴파일로 넘어갔습니다. 수정본은 Python 3.12 x64를 검사/선택하고 **미리 빌드된 Windows 설치 파일 25개를 포함**해 컴파일 없이 설치합니다.

1. [공식 Python 3.12 64비트 설치 파일](https://www.python.org/ftp/python/3.12.10/python-3.12.10-amd64.exe)로 설치합니다. Add python.exe to PATH와 Python Launcher를 선택하세요. 다른 Python을 삭제할 필요는 없습니다.
2. 위 **수정 ZIP** 전체를 새 폴더에 압축 해제합니다. 기존 폴더의 data에는 상품자료가 있으므로 기존 폴더는 보관하세요.
3. SH_Auto_Seller 폴더의 **START_WINDOWS.bat**을 실행합니다.

이전 가상환경을 그대로 사용하면 호환성을 확인하고, 비호환이면 백업 후 재생성합니다. Rust/Visual Studio 설치는 필요하지 않습니다.

## 검증과 범위

- 회귀/런타임/설치 해시 검사 테스트 **31개 통과**. 기존 브라우저 흐름 테스트 2개 통과.
- Windows CPython 3.12 x64 대상의 오프라인 의존성 해결과 해시 검증 통과.
- wheel SHA-256 25개 전부 공식 PyPI 릴리스 메타데이터와 일치 확인. 설치 시 pip 해시 검증도 유지합니다.
- 실제 Windows OS에서의 최종 실행은 아직 미검증입니다. AI·자동 수집·QAPI·QSM은 후속 단계이며 실제 등록은 차단됩니다.
- 전체 소스·빌드된 React 화면·한국어 안내·연습용 데모를 포함합니다. Node.js는 일반 실행에 필요하지 않습니다.
- API 키·비밀번호·.env·사용자 DB·가상환경은 제외했습니다.

파일 크기: 6,390,955 bytes

SHA-256: `07cc820613414beac5fb38178928a57eafc0cd0ff2575596a1e4e1ace16548a9`
