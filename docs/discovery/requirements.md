# Requirements

> Tai lieu nay la nguon du lieu duy nhat cho Buoc 03 (Product Brief).
> Moi thong tin deu da duoc human xac nhan hoac uy quyen cho AI quyet dinh trong pham vi MVP.
> Cap nhat lan cuoi: 2026-05-20T14:28:04.0552700+07:00

---

## 1. Tom tat du an

- **Ten du an**: Tech Trend
- **Mo ta mot cau**: Website tu dong thu thap, tong hop, va phan tich cac xu huong cong nghe tu nhieu nguon de hien thi cac bang xep hang va chi so tang truong.
- **Loai app**: Fullstack web application voi public web UI va admin web UI
- **Doi tuong su dung**: Nguoi dung guest muon theo doi xu huong cong nghe va admin quan ly nguon du lieu, trong so, va lich crawl

## 2. User Roles

| Role | Mo ta | Cach tao tai khoan | Quyen dac biet |
|---|---|---|---|
| Guest | Xem cac bang xep hang, chi so tang truong, va du lieu trend cong khai | Khong can tai khoan | Xem du lieu public, doi ngon ngu giao dien EN/VI |
| Admin | Cau hinh nguon du lieu va van hanh qua trinh thu thap, tong hop | Tai khoan admin duoc seed luc deploy | Bat/tat nguon, chinh trong so, fetch thu cong, xem log crawl |

> Co guest (chua dang nhap): Co

## 3. Tinh nang MVP (phai co cho launch)

- Bang xep hang AI model theo nhieu hang muc nhu coding, reasoning, speed, math, cost, elo va cac muc bo sung hop ly do AI de xuat cho MVP
- Bang xep hang cac du an cong nghe tren GitHub co tang truong nhanh, mac dinh uu tien tang star theo tuan
- He thong tong hop diem/xep hang AI model dua tren nhieu nguon va trong so theo tung nguon
- Tu dong crawl va cap nhat du lieu dinh ky moi 6 tieng
- Trang admin cho phep bat/tat nguon du lieu, chinh trong so, fetch ngay lap tuc, va xem log crawl
- Giao dien da ngon ngu EN+VI cho phan giao dien tinh

> Chi tiet tung tinh nang se duoc mo rong trong Product Brief.

## 4. Tinh nang Phase 2 (de sau)

- Toi uu mobile experience vuot muc co ban cho mobile browser
- Dich thuat dong cho thuat ngu bang xep hang hoac insight nang cao
- Tich hop them cac dich vu ngoai danh sach nguon tham khao ban dau neu can mo rong do bao phu
- Mo rong them cac dashboard, bo loc, va che do phan tich nang cao ngoai MVP

## 5. Du lieu & Do nhay cam

- **Loai du lieu**: Chu yeu la du lieu cong khai tu cac nguon ben ngoai va cau hinh van hanh noi bo cho admin
- **Ma hoa can thiet**: In-transit cho giao tiep he thong va bao ve thong tin dang nhap admin o muc co ban
- **Du lieu can mask trong log**: Thong tin dang nhap admin, token truy cap nguon neu co, va cac truong bi mat trong cau hinh ket noi

## 6. External Services

| Service | Muc dich | Da co contract/account? |
|---|---|---|
| GitHub | Thu thap du lieu du an cong nghe va chi so tang truong | Chua xac dinh |
| OpenRouter | Tham khao du lieu va bang xep hang AI model neu phu hop voi pham vi MVP | Chua xac dinh |
| LMArena | Tham khao du lieu danh gia AI model | Chua xac dinh |
| aibenchmarks | Tham khao benchmark va thong so xep hang AI model | Chua xac dinh |
| ArtificialAnalysis | Tham khao benchmark va so sanh AI model | Chua xac dinh |

## 7. Timeline & Team

- **Deadline du kien**: 1-2 tuan
- **Team size**: 1 nguoi dieu khien quy trinh voi ho tro cua Codex AI
- **Ghi chu ve team**: Can uu tien MVP scope gon, quyet dinh nhanh, va luong tu dong hoa cao trong qua trinh phat trien

## 8. Budget & Infrastructure

- **Hosting budget/thang**: Chay local trong giai doan hien tai
- **Cloud preference**: Khong ap dung o giai doan nay
- **Ghi chu**: Uu tien kha nang chay local on dinh va thoi gian trien khai nhanh

## 9. UI & Design

- **Co UI khong**: Co Web UI cho public va admin
- **Da ngon ngu**: Co (Tieng Anh + Tieng Viet)
- **Design source**: `DESIGN.md` co san o project root
- **Ghi chu design**: Thuat ngu bang xep hang giu tieng Anh; giao dien tinh ho tro EN/VI; chi tiet thi giac se lay tu `DESIGN.md`
- **Dark mode**: Chua quyet dinh

## 10. Domain-specific

- He thong phai tong hop xep hang AI model tu nhieu nguon va ap dung trong so theo tung nguon
- Trong so theo nguon can co gia tri mac dinh hop ly trong MVP, nhung admin co the dieu chinh sau
- Cac hang muc AI model can bao gom it nhat: coding, reasoning, speed, math, cost, elo; co the bo sung hang muc phu neu phu hop
- Logic GitHub trending tap trung vao tang truong theo tuan, ket hop nhieu chi so, va mac dinh sort theo tang star theo tuan
- Admin co the kich hoat fetch thu cong truoc ky cap nhat dinh ky 6 tieng
- Log crawl can duoc luu de admin kiem tra ket qua va su co thu thap du lieu

## 11. Rang buoc da biet

- Khong can toi uu mobile experience o muc cao trong MVP
- Du an phai hoan thanh trong 1-2 tuan nen can uu tien tinh nang cot loi va giam thieu scope phu
- Chi co 1 nguoi dieu khien quy trinh nen admin flow can don gian va van hanh de dang
- Giai doan hien tai uu tien chay local, chua yeu cau van hanh production tren ha tang ben ngoai

## 12. Known Unknowns (chua ro — se giai quyet sau)

| Cau hoi chua ro | Ke hoach giai quyet | Anh huong neu sai |
|---|---|---|
| Danh sach day du cac hang muc AI model trong MVP ngoai cac muc toi thieu | Chot tai Buoc 03 trong Product Brief va ADR lien quan den logic san pham | Co the lam bang xep hang thieu bao phu hoac qua rong so voi timeline |
| Gia tri trong so mac dinh cho tung nguon du lieu AI model | Quyet dinh tai Buoc 03 dua tren muc tieu MVP va kha nang du lieu | Anh huong truc tiep den tinh hop ly cua bang xep hang tong hop |
| Nguon du lieu cu the nao trong danh sach tham khao se duoc dua vao MVP | Chot tai Buoc 03 sau khi can doi do phuc tap va thoi gian trien khai | Anh huong den pham vi crawl, do on dinh, va toc do giao hang |
| Dark mode co nam trong MVP hay khong | Xac nhan tai Buoc 03 khi xem xet `DESIGN.md` va muc tieu UI | Anh huong den effort frontend va pham vi giao dien |

## 13. Cac assumption da chot voi human

| Assumption | Batch/cau | Anh huong |
|---|---|---|
| Website khong can toi uu mobile experience o muc cao trong MVP | Batch 1, cau 1 | Cho phep uu tien desktop-first va giam scope UI responsive nang cao |
| Guest duoc xem du lieu public, admin la role van hanh duy nhat | Batch 1, cau 2 | Don gian hoa phan quyen va auth trong MVP |
| MVP uu tien bang xep hang AI model, GitHub tech projects, admin config, crawl tu dong, va EN+VI | Batch 1, cau 3 | Xac dinh scope launch va loai bo tinh nang ngoai pham vi |
| Team 1 nguoi voi Codex AI va timeline 1-2 tuan | Batch 1, cau 4 | Bat buoc scope gon va tu dong hoa cao |
| He thong khong xu ly du lieu nhay cam dang ke; auth admin co the o muc don gian | Batch 2, cau 5 | Giam do phuc tap bao mat cho MVP nhung van can bao ve thong tin dang nhap co ban |
| Danh sach nguon tham khao co the duoc chon linh hoat theo do phuc tap va thoi gian trien khai | Batch 2, cau 6 | Cho phep toi uu pham vi crawl trong Buoc 03 |
| Giai doan hien tai chi can chay local | Batch 2, cau 7 | Chua can toi uu chi phi hosting hay ha tang van hanh ben ngoai |
| `DESIGN.md` la nguon dinh huong thiet ke chinh | Batch 2, cau 8 | Buoc 03 va cac buoc sau can doc file nay thay vi tu suy doan style |
| Trong so theo nguon du lieu AI model co the cau hinh qua admin, voi mac dinh do AI quyet dinh cho MVP | Batch 3, cau 1-2 | Yeu cau co giao dien va logic quan tri trong so |
| GitHub trending mac dinh theo tang star theo tuan, nhung co the sort theo kieu khac | Batch 3, cau 3 | Dinh huong logic xep hang va bo loc cua bang GitHub |
| Crawl tu dong moi 6 tieng va admin co nut fetch ngay | Batch 3, cau 4 | Xac dinh yeu cau scheduling va thao tac thu cong |
| Admin can bat/tat nguon, chinh trong so, fetch, va xem log crawl | Batch 3, cau 5 | Dinh nghia pham vi admin MVP |
| EN+VI chi ap dung cho giao dien tinh; thuat ngu bang xep hang giu tieng Anh | Batch 3, cau 6 | Giam do phuc tap localization cho noi dung du lieu |
