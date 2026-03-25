{%- set all_passed = (results_table | selectattr("passed") | length) == (results_table | length) %}

{%- if all_passed %}

## 단계 {{ step_number }} - 통과 ✅

{%- else %}

## 단계 {{ step_number }} - 실패 ❌

{%- endif %}

{%- if all_passed %}
<img src="https://octodex.github.com/images/inflatocat.png" align="right" height="150px" alt="단계 통과를 나타내는 Inflatocat 이미지" />
{%- else %}

<img src="https://octodex.github.com/images/spidertocat.png" align="right" height="100px" alt="단계 실패를 나타내는 Spidertocat 이미지" />
일부 검사가 실패했습니다. 아래 결과를 확인하고 다시 시도해 주세요.

버그를 찾아봅시다! 🤔
{%- endif %}

| 상태 | 설명 |
| --- | --- |

{%- for row in results_table %}
| {% if row.passed -%}✅ - 통과{%- else -%}❌ - 실패{%- endif %} | {{ row.description }} |
{%- endfor %}

{%- if tips and tips.length %}

### 팁

{%- for tip in tips %}

- {{ tip }}
  {%- endfor %}

{%- endif %}
