# PVZ-Scared — Bản Việt Hóa 🇻🇳

**Việt hóa bởi: [Elainabaka](https://github.com/Elainabaka)**

Bản Việt hóa hoàn chỉnh cho fan-game **PVZ-Scared** (*Plants vs. Zombies* bản kinh dị).
Tải về, giải nén, chạy `PVZ-Scared.exe` là chơi ngay — không cần cài đặt.

> 🎮 **Game gốc (bản Trung, chính chủ):** <https://pvzscared.com/> —
> trang web của team phát triển, có đủ bản PC/Android/iOS.
> Bản này chỉ khác ở chỗ đã dịch toàn bộ sang tiếng Việt.

---

## 📥 Cách chơi

1. Tải file ZIP của bản Việt hóa về, giải nén ra một thư mục
   (giữ nguyên cấu trúc bên trong, đừng xóa file nào).
2. Chạy **`PVZ-Scared.exe`**.
3. Chọn ngôn ngữ **Tiếng Việt** trong phần Cài đặt → Ngôn ngữ của game
   (nếu game đã hiện tiếng Việt sẵn thì cứ thế chơi thôi).

> 💡 Lần đầu chạy, Windows có thể hiện cảnh báo SmartScreen — chọn
> *More info → Run anyway* (game offline, không mạng, không virus).

## ✅ Có gì trong bản Việt hóa này

- **325 chuỗi** menu, mô tả cây/zombie, cửa hàng, hộp thoại… dịch đầy đủ dấu.
- **Phụ đề radio** (bản tin Tiếng Nói Ngoại Ô) và **Nhật ký** (Diary) dịch hoàn chỉnh.
- **Chuỗi UI cứng** trong scene (nút bấm, tiêu đề, cài đặt, độ khó, tỉ lệ…) — bổ sung dấu +
  dịch nốt những chỗ còn sót tiếng Trung (`Đóng`, `Trang 1`, `Người dùng mặc định`,
  `Nhập tên của bạn:`, `Màn 1-1`, `Tốc độ:`, `Độ sáng`, `Nắng:`, `Hồi:`…).
- **Sửa lỗi font chữ tiếng Việt**: nạp font dự phòng (fallback) vào toàn bộ font hiển thị
  của game nên chữ có dấu (ế, ộ, ữ, đ, ă, ơ, ư…) hiện đầy đủ, không còn ô vuông/mất chữ.
- Tiêu đề cửa sổ game đã đổi sang tiếng Việt.

## 🆕 Có gì mới ở bản v1.3 (bản hoàn chỉnh)

- **Chống cắt dấu trên/dưới trong font** (lỗi ẩn khó thấy): 11 font được vá metric
  (`head.yMax`, `usWinAscent`/`usWinDescent`) theo bounding-box thật của **chữ tiếng Việt** —
  dấu chồng của ế, ộ, ử khòng còn nguy cơ bị "mất đầu dấu" ở renderer theo chuẩn WinGDI.
  Glyph ghép cũng được tính lại bbox (trước đó còn giữ giá trị cũ theo font gốc).
- **Vá nớt tên 6 màn mở đầu còn sót tiếng Trung**: `序章-1…5, 41` → `Màn 0-1…5, 41`,
  mô tả `无` → `Không` (đồng bộ với 35 màn còn lại).
- **Rà soát toàn bộ lần cuối trước khi phát hành**: 325 chuỗi ngôn ngữ khớp 1:1 với bản nhúng
  trong game, 0 sót chữ Trung trong chuỗi hiển thị, 0 lỗi placeholder/thị định dạng/Unicode
  (NFC), phụ đề radio + nhật ký + dữ liệu màn đều là tiếng Việt.

## 🆕 Có gì mới ở bản v1.2 (so với v1.1)

- **Sửa lỗi font "chữ to chữ bé"**: 8 font trang trí (fzkt1, 方正艺黑, 方正简体剪纸,
  ark-pixel, PerfectDOS, fzcq, fzjz1, fangzhengkatong) được **dựng lại từ font gốc**:
  glyph tiếng Việt giờ scale đúng theo unitsPerEm từng font, advance/căn giữa chuẩn,
  hết hiện tượng chữ Việt nhỏ hơn/thấp hơn chữ Latin, hết chồng chữ.
- **Vá 6 font bị hỏng bảng `vmtx`** (fonttools báo lỗi đọc) — loại bỏ bảng hỏng.
- **Hết ô vuông (tofu)**: bỏ kaomoji `(｡･ω･｡)ﾉ♡` cuối màn cảnh báo (font game không có
  glyph `｡ ﾉ ♡`) → thay bằng `(^_^)`. Log game không còn cảnh báo thiếu ký tự.
- **Sửa chuỗi hiển thị sai**: `Tỷ lệ nhân năng` → `Tỷ lệ nắng`, `Bắt chớp mắt` →
  `Bật chớp mắt`, `Nhấn đúp thẻ đổi trạng thái mạng` → `Nhấn đúp thẻ để bật/tắt mang theo`,
  `quyền quẹt thẻ` → `quyền trả tiền`, `kích phát` → `gây ra`.
- **Dịch nốt chữ Anh sót trong credit**: `Art` → `Mỹ thuật`, `Code` → `Lập trình`,
  `F-Scr` → `Kịch bản`.
- **Dọn chuỗi test rác**: `Mô tả thử…`, `Thử thử…`, `Nội dung thử nghiệm…`, `Tên thử`,
  `Nhập văn bản` → thay bằng câu tiếng Việt hoàn chỉnh.
- Chuỗi UI cứng & file ngôn ngữ nhúng (`Resources/Json/Languages/zh.json`) đã được vá
  đồng bộ với `External/Language/vi.json`.

## 🆕 Có gì mới ở bản v1.1 (so với v1.0.1)

- **Merge glyph tiếng Việt vào font gốc**: 8 font trang trí của game (fzkt1, 方正艺黑,
  方正简体剪纸, ark-pixel, PerfectDOS, fzcq, fzjz1, fangzhengkatong) giờ đã có sẵn
  chữ Việt đúng kiểu chữ gốc — hết hiện tượng chữ Việt rớt sang font khác (lệch kiểu)
  ở menu Cài đặt, màn hình tên người chơi, nhật ký…
- **Màn cảnh báo đầu game đọc ngon**: chữ disclaimer hết dấu rời (`l ò ng` → `lòng`),
  credit UP chủ Bilibili giữ nguyên ý nghĩa (bỏ nickname chữ Tàu vì font game không vẽ được).
- **Vẽ lại 8 ảnh nút/banner chữ Tàu** theo phong cách gốc: `CHUẨN BỊ…`, `SẴN SÀNG…`,
  `TRỒNG CÂY!` (mở màn), `ĐỢT CUỐI!`, `ĂN!`, banner `SINH TỒN`, biển `CHÀO MỪNG, BẠN!`.
- Vá chuỗi lẻ: ngoặc Tàu `（）` → `()`, `dồn dame` → `dồn sát thương`, `——` → `—`,
  thay chuỗi test rác bằng tiếng Việt.

## ⚠️ Vài điểm còn chưa hoàn hảo (sẽ sửa ở bản sau)

- Hộp thoại **"版本检测失败 / 无法连接到服务器…"** khi máy offline (game check server lúc mở)
  là chuỗi **hardcode trong code game** (metadata IL2CPP đã mã hoá) — không thể dịch bằng
  cách vá asset, cần hook runtime ở bản sau.
- Logo chữ Tàu ở menu chính được **giữ nguyên** (nhận diện thương hiệu của team gốc).
- Nút **Bỏ qua** (Skip) ở màn nhật ký/cốt truyện vẫn là ảnh nút tiếng Trung `跳过`
  (chữ vẽ sẵn trong texture, cần vẽ lại ảnh — không phải lỗi font).
- Chữ khắc trên bia mộ / bùa giấy và nickname thành viên team (chữ Tàu trang trí)
  được giữ nguyên theo bản gốc.
- Tên riêng của team phát triển và các nickname (Bilibili/TikTok) được **giữ nguyên**
  để tôn trọng tác giả gốc (nickname UP chủ trong game đã gọn lại thành
  "tác giả gốc" vì font game không vẽ được chữ Tàu — credit đầy đủ ở đây).

## 🙏 Credit

- **Game gốc**: team phát triển Trung Quốc (UP chủ Bilibili *"对不起贱笑了"*,
  lập trình @道源君Tao cùng các họa sĩ/nhạc sĩ trong nhóm) —
  fan-game miễn phí, phóng tác từ IP *Plants vs. Zombies*.
  Link chính chủ: <https://pvzscared.com/>
- **Việt hóa**: **[Elainabaka](https://github.com/Elainabaka)**.
- Cảm ơn các tác giả font/mỹ thuật của game gốc.

## 📜 Tuyên bố

- Game gốc **hoàn toàn miễn phí, không có nạp tiền** — bản Việt hóa này cũng vậy.
- *Plants vs. Zombies* thuộc bản quyền EA/PopCap. Đây là bản dịch cộng đồng,
  **phi thương mại, phục vụ mục đích học tập & giải trí**. Nếu tác giả gốc hoặc
  chủ sở hữu IP yêu cầu gỡ, mình sẽ gỡ ngay.
- Vui lòng không dùng bản này để kinh doanh, thu phí hay re-upload kiếm tiền.

## 🖥️ Cấu hình

- Windows 10/11 64-bit, RAM 4GB+, card đồ họa bất kỳ chạy được Unity.
- Độ phân giải khuyến nghị 1920×1080.

---
*Dịch bằng cả tâm huyết — chúc anh em chơi vui, đừng để zombie gặm não! 🧟‍♂️🌻*
