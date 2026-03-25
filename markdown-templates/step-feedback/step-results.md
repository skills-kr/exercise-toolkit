{{#passed}}
## Step {{ step_number }} - 통과 ✅
{{/passed}}
{{^passed}}
## Step {{ step_number }} - 실패 ❌
{{/passed}}

{{#passed}}
<img src="https://octodex.github.com/images/inflatocat.png" align="right" height="200px" />
{{/passed}}
{{^passed}}
<img src="https://octodex.github.com/images/spidertocat.png" align="right" height="100px" />
일부 검사에 실패했습니다. 아래 결과를 검토하고 다시 시도하세요.

버그를 찾아보세요! 🤔
{{/passed}}

| 상태 | 이름 | 메시지 |
| --- | --- | --- |
{{#results_table}}
| {{#passed}}✅ - 통과{{/passed}}{{^passed}}❌ - 실패{{/passed}} | {{ name }} | {{ message }} |
{{/results_table}}

{{#tips.length}}
### 팁

{{#tips}}
- {{.}}
{{/tips}}
{{/tips.length}}
