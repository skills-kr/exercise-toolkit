{{#passed}}

## 단계 {{ step_number }} - 통과 ✅

{{/passed}}
{{^passed}}

## 단계 {{ step_number }} - 실패 ❌

{{/passed}}

{{#passed}}
<img src="https://octodex.github.com/images/inflatocat.png" align="right" height="150px" alt="단계 통과를 나타내는 Inflatocat 이미지" />
{{/passed}}
{{^passed}}
<img src="https://octodex.github.com/images/spidertocat.png" align="right" height="100px" alt="단계 실패를 나타내는 Spidertocat 이미지" />
일부 검사가 실패했습니다. 아래 결과를 확인하고 다시 시도해 주세요.

버그를 찾아봅시다! 🤔
{{/passed}}

| 상태 | 설명 |
| --- | --- |
{{#results_table}}
| {{#passed}}✅ - 통과{{/passed}}{{^passed}}❌ - 실패{{/passed}} | {{ description }} |
{{/results_table}}

{{#tips.length}}

### 팁

{{#tips}}

- {{.}}
  {{/tips}}
  {{/tips.length}}
