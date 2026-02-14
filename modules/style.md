# 스타일 모듈

## HTML/Table 레이아웃 패턴
```md
<table>
  <tr>
    <td valign="top" width="55%">
      <!-- 왼쪽 컬럼 콘텐츠 -->
    </td>
    <td valign="top" width="45%">
      <!-- 오른쪽 컬럼 콘텐츠 -->
    </td>
  </tr>
</table>
```

## 중앙 정렬 래퍼
```md
<p align="center">
  <!-- 중앙 정렬 위젯/이미지 -->
</p>
```

## 이미지 높이 팁
- 나란히 배치한 카드 높이는 동일하게 유지 (`height="160"`).
- SVG 카드 병렬 배치 시 높이를 명시해 정렬을 안정화.
- 로컬 리소스는 상대 경로 사용 (예: `./assets/metrics.svg`).
