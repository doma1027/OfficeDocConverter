좋습니다. 말씀하신 대로 **“변환만 한다”**라는 목적에 맞춰 README를 더 단순하고 명확하게 정리했습니다.

---

# 오피스 문서 **일괄 변환 도구**

(Batch Office Document Converter)

> **목적**
> **MS 오피스(Word, Excel, PowerPoint)**와 **한컴오피스(한글, 한셀, 한쇼, 한워드)**가 지원하는 문서를
> 지정한 폴더 단위로 탐색하여 **다른 형식으로 일괄 변환**하는 도구입니다.

---

## 주요 기능

* **폴더 단위 변환**: 지정한 폴더(하위 포함)의 문서를 자동 탐색 후 일괄 변환
* **포맷 라우팅**: 문서 형식에 따라 적합한 앱(Word, Excel, PowerPoint, Hwp, HCell, HShow, HWord)을 자동 호출
* **다양한 출력 형식 지원**:

  * Word/HWord: DOCX, RTF, TXT, PDF …
  * Excel/HCell: XLSX, CSV, PDF …
  * PowerPoint/HShow: PPTX, PDF …
  * 한글(Hwp/HwpX): HWPX, PDF, DOCX …
* **안정적 실행**: 문서별 타임아웃/재시도, 주기적 엔진 재기동으로 대량 변환 지원
* **로그 기록**: 변환 성공/실패, 소요 시간, 오류 메시지 등을 CSV/JSON으로 저장

---

## 폴더 구조(예시)

```
project-root/
 ├─ IN/                         # 입력 문서 루트
 ├─ OUT/
 │   ├─ DOCX/ CSV/ PPTX/ PDF/   # 출력 형식별 폴더
 │   └─ logs/                   # 변환 로그
 └─ CONFIG/
     └─ app-settings.json       # 변환 옵션(형식, 타임아웃 등)
```

---

## 실행 흐름

1. **대상 폴더 선택**
2. **출력 형식 지정** (예: DOCX, PDF, CSV 등)
3. **실행 버튼 클릭 → 자동 변환 진행**
4. **OUT 폴더에서 변환된 결과 확인**
5. **로그 파일로 성공/실패 내역 검토**

---

## 로그 항목 (예시)

* `input_path` : 원본 파일 경로
* `input_ext` : 원본 확장자
* `app_used` : 변환에 사용된 앱 (word/excel/ppt/hwp/hcell/hshow/hword)
* `output_format` : 변환된 형식
* `output_path` : 출력 파일 경로
* `status` : SUCCESS / FAIL / RETRY
* `elapsed_ms` : 변환 소요 시간(ms)
* `error_message` : 오류 발생 시 메시지

---

## 시스템 요구사항

* **OS**: Windows 10/11
* **필수**: MS Office(Word/Excel/PowerPoint), 한컴오피스(한글/한셀/한쇼/한워드) 정품 설치
* **폰트/언어팩**: 변환 대상 문서에 필요한 리소스 사전 설치

---

### 한 줄 요약

**여러 오피스 제품군의 문서를 지정한 폴더 단위로 탐색해 원하는 형식으로 일괄 변환하는 전용 도구**입니다.

---

원하시면 이 README에 **지원 입력/출력 형식 표**(예: “DOCX → PDF, RTF, TXT” 같은 매트릭스 형태)를 추가해드릴 수도 있는데, 넣어드릴까요?
