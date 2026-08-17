# Lab 17 Golden Set Report

- Implementation: `student`
- Kind: `golden`
- Cases: **20**
- Passed: **20/20**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **827.5 ms**
- Average token reduction vs full source context: **6.3%**
- Golden bonus: **10/10** (100% required)

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| G01 | short_term | PASS | 0.2 | 227 | 0.0% |  |
| G02 | short_term | PASS | 0.0 | 133 | 0.0% |  |
| G08 | long_term | PASS | 1252.1 | 829 | 0.0% |  |
| G09 | long_term | PASS | 1200.6 | 1393 | 0.0% |  |
| G12 | semantic | PASS | 223.6 | 418 | 8.9% |  |
| G14 | semantic | PASS | 206.8 | 270 | 30.2% |  |
| G15 | semantic | PASS | 220.1 | 270 | 41.2% |  |
| G19 | mixed | PASS | 1321.7 | 581 | 0.0% |  |
| G03 | long_term | PASS | 1354.6 | 1398 | 0.0% |  |
| G04 | long_term | PASS | 1152.1 | 1394 | 0.0% |  |
| G05 | long_term | PASS | 1173.0 | 1374 | 0.0% |  |
| G10 | episodic | PASS | 221.9 | 582 | 0.0% |  |
| G11 | episodic | PASS | 215.7 | 588 | 0.0% |  |
| G13 | semantic | PASS | 220.7 | 416 | 26.4% |  |
| G16 | mixed | PASS | 1380.3 | 581 | 0.0% |  |
| G18 | mixed | PASS | 472.7 | 500 | 11.5% |  |
| G20 | mixed | PASS | 1657.6 | 831 | 0.0% |  |
| G06 | long_term | PASS | 1244.8 | 1391 | 0.0% |  |
| G07 | long_term | PASS | 1541.6 | 1376 | 0.0% |  |
| G17 | mixed | PASS | 1489.0 | 581 | 8.1% |  |

## Evidence excerpts

### G01 - short_term

`<SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. | assistant: Noted staging constraint. | user: Filler A about button padding. | assistant: Filler A. | user: Filler B about color tokens. | assistant: Filler B. | user: Filler C about copy tone. | assistant: Filler C. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. - user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. - assistant: Noted staging constraint. </DURA`

### G02 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### G08 - long_term

`<USER_SUMMARY> Lan's project is LOTUS-88, and they use Java and Spring Boot for backend examples. They do not use Python for the backend. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend.   - Created At: 2026-08-01 11:00:20     Source: message     Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples.   - Creat`

### G09 - long_term

`<USER_SUMMARY> Minh Nguyen's personal project is named ORCHID-27, for which Python is used. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project.  Minh Nguyen prefers Python and dislikes Java. When explaining code, Minh prefers short examples. The user is currently learning about async/await and sometimes confuses coroutines with Tasks. If this topic arises in the future, the user wants explanations to be provided as a timeline. The user prefers Python for personal demos (ORCHID-27) but requires TypeScript with NestJS for the BLUEBIRD-42 company project's backend.  The assistant will prioritize a timeline when explain`

### G12 - semantic

`EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} metadata= EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. metadata= EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal `

### G14 - semantic

`EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. metadata= EPISODE: {"id":"kb-context-budget","entity":"Memory Context Budget","summary":"Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodi`

### G15 - semantic

`EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. metadata= EPISODE: {"id":"kb-context-budget","entity":"Memory Context Budget","summary":"Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodi`

### G19 - mixed

`<LONG_TERM> <USER_SUMMARY> Lan's project is LOTUS-88, and they use Java and Spring Boot for backend examples. They do not use Python for the backend. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-17 14:26:20     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Evaluation User" }: Lan uu tien stack backend nao cho LOTUS-88?   - Created At: 2026-08-01 11:00:20     Source: message     Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples.   - Created At: 2026-08-01 11:00:00     Source: message     `

### G03 - long_term

`<USER_SUMMARY> Minh Nguyen's personal project is named ORCHID-27, for which Python is used. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project.  Minh Nguyen prefers Python and dislikes Java. When explaining code, Minh prefers short examples. The user is currently learning about async/await and sometimes confuses coroutines with Tasks. If this topic arises in the future, the user wants explanations to be provided as a timeline. The user prefers Python for personal demos (ORCHID-27) but requires TypeScript with NestJS for the BLUEBIRD-42 company project's backend.  The assistant will prioritize a timeline when explain`

### G04 - long_term

`<USER_SUMMARY> Minh Nguyen's personal project is named ORCHID-27, for which Python is used. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project.  Minh Nguyen prefers Python and dislikes Java. When explaining code, Minh prefers short examples. The user is currently learning about async/await and sometimes confuses coroutines with Tasks. If this topic arises in the future, the user wants explanations to be provided as a timeline. The user prefers Python for personal demos (ORCHID-27) but requires TypeScript with NestJS for the BLUEBIRD-42 company project's backend.  The assistant will prioritize a timeline when explain`

### G05 - long_term

`<USER_SUMMARY> Minh Nguyen's personal project is named ORCHID-27, for which Python is used. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project.  Minh Nguyen prefers Python and dislikes Java. When explaining code, Minh prefers short examples. The user is currently learning about async/await and sometimes confuses coroutines with Tasks. If this topic arises in the future, the user wants explanations to be provided as a timeline. The user prefers Python for personal demos (ORCHID-27) but requires TypeScript with NestJS for the BLUEBIRD-42 company project's backend.  The assistant will prioritize a timeline when explain`

### G10 - episodic

`EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. EPISODE: Toi se uu tien timeline khi giai thich coroutine va Task. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Da ghi nh`

### G11 - episodic

`EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + con`

### G13 - semantic

`EPISODE: {"id":"kb-async-http","entity":"Async HTTP Incident Playbook","summary":"When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST.","source":"incident-playbook-2026","updated_at":"2026-08-11T00:00:00Z"} metadata= EPISODE: When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST. metadata= EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data witho`

### G16 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh Nguyen's personal project is named ORCHID-27, for which Python is used. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project.  Minh Nguyen prefers Python and dislikes Java. When explaining code, Minh prefers short examples. The user is currently learning about async/await and sometimes confuses coroutines with Tasks. If this topic arises in the future, the user wants explanations to be provided as a timeline. The user prefers Python for personal demos (ORCHID-27) but requires TypeScript with NestJS for the BLUEBIRD-42 company project's backend.  The assistant will prioritize a timeline `

### G18 - mixed

`<EPISODIC> EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo `

### G20 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh Nguyen's personal project is named ORCHID-27, for which Python is used. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project.  Minh Nguyen prefers Python and dislikes Java. When explaining code, Minh prefers short examples. The user is currently learning about async/await and sometimes confuses coroutines with Tasks. If this topic arises in the future, the user wants explanations to be provided as a timeline. The user prefers Python for personal demos (ORCHID-27) but requires TypeScript with NestJS for the BLUEBIRD-42 company project's backend.  The assistant will prioritize a timeline `

### G06 - long_term

`<USER_SUMMARY> Minh Nguyen's personal project is named ORCHID-27, for which Python is used. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project.  Minh Nguyen prefers Python and dislikes Java. When explaining code, Minh prefers short examples. The user is currently learning about async/await and sometimes confuses coroutines with Tasks. If this topic arises in the future, the user wants explanations to be provided as a timeline. The user prefers Python for personal demos (ORCHID-27) but requires TypeScript with NestJS for the BLUEBIRD-42 company project's backend.  The assistant will prioritize a timeline when explain`

### G07 - long_term

`<USER_SUMMARY> Minh Nguyen's personal project is named ORCHID-27, for which Python is used. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project.  Minh Nguyen prefers Python and dislikes Java. When explaining code, Minh prefers short examples. The user is currently learning about async/await and sometimes confuses coroutines with Tasks. If this topic arises in the future, the user wants explanations to be provided as a timeline. The user prefers Python for personal demos (ORCHID-27) but requires TypeScript with NestJS for the BLUEBIRD-42 company project's backend.  The assistant will prioritize a timeline when explain`

### G17 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh Nguyen's personal project is named ORCHID-27, for which Python is used. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project.  Minh Nguyen prefers Python and dislikes Java. When explaining code, Minh prefers short examples. The user is currently learning about async/await and sometimes confuses coroutines with Tasks. If this topic arises in the future, the user wants explanations to be provided as a timeline. The user prefers Python for personal demos (ORCHID-27) but requires TypeScript with NestJS for the BLUEBIRD-42 company project's backend.  The assistant will prioritize a timeline `
