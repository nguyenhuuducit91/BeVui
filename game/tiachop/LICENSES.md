# Hình của trò "Biệt đội Tia Chớp" – nguồn gốc

Tạo ngày 22/11/2026 bằng **FLUX.1-schnell** (Black Forest Labs, giấy phép Apache-2.0 – dùng thương mại được) trên Google Colab (`tools/game-art/gen_colab.py`); tách nền bằng rembg (MIT) hoặc theo nền trắng. Chủ dự án chọn bản dùng (docs/thiet-ke/tiachop/yeu-cau-my-thuat.md §5, §7). Xuất bằng `tools/game-art/export_picks.py`.

| Tệp | Ảnh gốc (đợt/tệp) | Câu lệnh |
|---|---|---|
| `nen/troi.webp` | art-job-02/l1_sky2_v1 |  |
| `nen/rung-xa.webp` | art-job-01/l1_far_v1 |  |
| `nen/cot-da.webp` | art-job-02/mid_pillar_v2 |  |
| `giao-dien/vien-nang.webp` | art-job-02/pickup_capsule_v2 |  |

`nen/dat/*.webp` (mặt đất, bệ đá) dựng lại từ `nen/manh/be-da-2-*` (chính các ảnh trên) bằng `tools/game-art/make_ground.py`: cắt phần đá sạch, là phẳng mặt cỏ.

`nen/cay/*.webp` (cây lớp giữa): art-job-03, FLUX.1-schnell (Apache-2.0), đợt "canh" trong `tools/game-art/art_jobs.py` – cay-da-1 ← tree_banyan_v1, cay-da-2 ← tree_banyan_v2, cay-cao ← tree_tall_v1, dua-1 ← tree_palm_v1, dua-2 ← tree_palm_v3, duong-xi-1 ← tree_fern_v1, duong-xi-2 ← tree_fern_v2.

## Nhân vật 3D (khung hình)

`nhan-vat/khang/*.webp`, `nhan-vat/vy/*.webp`, `nhan-vat/frames.json`: kết xuất bằng Blender từ `tools/game-art/hero3d.py`, xuất bởi `tools/game-art/export_3d.py`.
Nguồn mô hình và động tác (CC0 1.0, dùng thương mại được, không bắt buộc ghi công – ghi để tiện tra): **Quaternius** – *Universal Base Characters [Standard]* (thân Superhero, chỉnh tỉ lệ thiếu niên) và *Universal Animation Library [Standard]* (động tác). Đầu, mắt, tóc, kính, ba lô, găng phát sáng, đệm vai, thắt lưng do script dựng. Màu theo hình 2D đã duyệt (`nhan-vat/*-chuan.webp`).


**24/11/2026:** nhân vật (lính) và robot (lính, tháp pháo, tháp nấm, drone, trùm Cua) không còn là ảnh: được vẽ bằng mã trong `src/games/tiachop/rig.ts` và `robots.ts` (thiết kế riêng, không cần giấy phép ảnh). Các ảnh nhân vật, robot, ảnh tiêu đề và mảnh nền không dùng đã xóa khỏi thư mục này (nguồn vẫn ở `docs/thiet-ke/tiachop/`).

**Âm thanh (24/11/2026):** toàn bộ tiếng động và nhạc nền của trò được tổng hợp bằng mã trong `src/games/tiachop/audio.ts` (Web Audio), không dùng tệp âm thanh nào.
