# Lab 17 Submission

## Kết quả và phân tích benchmark

Practice đạt 11/11 (100%); vì vậy không có layer yếu nhất: short-term 2/2, long-term 4/4, episodic 2/2, semantic 2/2 và mixed 1/1 đều đạt 100%. Golden đạt 20/20. No-memory chỉ đạt 2/11 (18,18%), là hai case short-term còn evidence trong thread.

E02 retrieve nhiều nhất với 1.398 token. E07 phải kết hợp long-term user preference (`Python`) và semantic payment policy (`Idempotency-Key`); thiếu một trong hai evidence thì không thể cá nhân hóa mà vẫn đúng quy tắc domain.

Memory-enabled giảm trung bình 14,19% token so với full source, trong khi no-memory giảm 81,82%. Reduction cao của no-memory không phải chất lượng tốt: nó rẻ vì trả evidence rỗng và làm hit rate giảm còn 18,18%. Cần đọc token efficiency cùng retrieval hit rate.

## Câu hỏi thực hành

Trong bộ test này, long-term quan trọng nhất vì quyết định nhiều case nhất (E02, E03, E08, E09), gồm cross-session recall, open loop, recency và user isolation. E08 cho thấy constraint mới theo project (`BLUEBIRD-42` dùng TypeScript/NestJS) ghi đè preference Python trong scope công ty, nhưng không xóa preference Python của `ORCHID-27`.

Zep Context Block/graph quản lý extraction, relevance, provenance và cross-session memory, giảm công sức orchestration; đổi lại phụ thuộc dịch vụ, latency và cách Zep chuẩn hóa evidence. Redis+Qdrant cho quyền kiểm soát schema, TTL, ranking và hạ tầng, nhưng phải tự làm extraction, conflict resolution, isolation, deletion verification và kết hợp keyword/vector retrieval.

Guardrail chống memory poisoning: chỉ durable-write khi user đã opt-in; validate scope/type theo schema; lưu source, timestamp, confidence và validity; yêu cầu review cho preference có tác động cao; không cho retrieved text hoặc heartbeat tự cấp quyền ghi. Khi conflict, ưu tiên fact mới đúng scope nhưng giữ provenance; mọi xóa user-scoped phải verify trên tất cả store.

E10 chứng minh compaction vẫn giữ `REVIEW-DEADLINE-1600`, Friday và `16:00` trong durable notes dù raw turn cũ bị evict. Buffer giữ nguyên transcript nhưng tăng token không giới hạn và làm evidence quan trọng bị chìm trong nhiễu.
