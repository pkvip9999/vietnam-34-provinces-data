---
license: cc-by-4.0
language:
- vi
- en
pretty_name: Vietnam 34 provinces statistics (after the 1 July 2025 merger)
size_categories:
- 100K<n<1M
task_categories:
- tabular-regression
- time-series-forecasting
tags:
- vietnam
- official-statistics
- provinces
- demographics
- economics
configs:
- config_name: default
  data_files: data/du-lieu-34-tinh.csv
---

# Số liệu thống kê 34 tỉnh, thành phố Việt Nam / Vietnam 34-province statistics

Bộ dữ liệu của **[Vietnam in Data](https://vietnamindata.com)**: 199 chỉ tiêu thống kê nhà nước (dân số, diện tích, GRDP, thu nhập,
lao động, doanh nghiệp, nông nghiệp, giáo dục, y tế…) theo **34 tỉnh, thành phố sau sáp nhập 1/7/2025**, 6 vùng và cả nước,
chuỗi 1988–2025, 106,294 dòng. Số các năm trước 2025 được quy về địa giới 34 tỉnh.

*English:* 199 official indicators for Vietnam's 34 provinces (after the 1 July 2025 merger), 6 regions and the
whole country, 1988–2025. Figures for years before the merger are re-aggregated to the new boundaries and flagged.

- Trang web, biểu đồ, bảng xếp hạng / Website, charts, rankings: <https://vietnamindata.com>
- Phương pháp / Methodology: <https://vietnamindata.com/phuong-phap>
- Tải từng chỉ tiêu / Per-indicator CSV: <https://vietnamindata.com/tai-ve>
- Nguồn gốc / Original source: Cục Thống kê (General Statistics Office / National Statistics Office of Vietnam), <https://www.nso.gov.vn>

## Tệp / Files

| Tệp | Nội dung |
|---|---|
| `data/du-lieu-34-tinh.csv` | Dạng dài: một dòng = chỉ tiêu × địa phương × kỳ / long format, one row per indicator × area × period |
| `data/chi-tieu.csv` | Từ điển chỉ tiêu: tên, đơn vị, nhóm, hướng (cao là tốt / thấp là tốt), quy tắc gộp, bảng nguồn, URL |
| `data/dia-phuong.csv` | 34 tỉnh + 6 vùng + cả nước: mã hành chính, vùng, tỉnh cũ hợp thành, URL |

Cột của `du-lieu-34-tinh.csv`: `chi_tieu` (mã), `ten_chi_tieu`, `don_vi`, `ma_dia_phuong` (mã tỉnh 2 chữ số, `V34-n` cho vùng,
`VN`), `cap` (`tinh` / `vung` / `ca_nuoc`), `dia_phuong`, `ky` (`Y2025` năm, `Q2026-3` quý, `M2026-09` tháng), `tan_suat`,
`nam`, `gia_tri`, `co` (mã cờ, dưới), `nguon` (dưới), `url` (trang của số đó trên Vietnam in Data).

### Mã cờ / Flags (`co`)

- `p`: sơ bộ / preliminary
- `e`: ước tính / estimate
- `i`: dự án tự tính (ghép tỉnh cũ) / computed by the project
- `b`: đứt chuỗi / series break
- `u`: độ tin cậy thấp / low reliability
- `d`: định nghĩa khác / different definition

### Nguồn của số / Origin (`nguon`)

- `cong_bo_34`: Cục Thống kê công bố theo 34 tỉnh / published by NSO for the 34 provinces
- `cong_bo_63`: Cục Thống kê công bố, địa giới không đổi / published by NSO, unchanged boundaries
- `tinh_lai`: dự án ghép từ các tỉnh cũ theo quy tắc gộp / aggregated by the project from former provinces
- `suy_ra`: suy ra = GRDP bình quân đầu người × dân số / derived = GRDP per capita × population

Số `tinh_lai` (cờ `i`) **không phải số chính thức**: dự án cộng / tính bình quân gia quyền số của các tỉnh cũ theo quy tắc ghi
ở trang phương pháp. Số chính thức theo 34 tỉnh của Cục Thống kê luôn được ưu tiên khi có.

## Trích dẫn / Citation

> Vietnam in Data (2026). *Số liệu thống kê 34 tỉnh, thành phố Việt Nam* (bản 2026-11-13). Xử lý từ số liệu của Cục Thống kê. https://vietnamindata.com

Khi dùng lại, ghi nguồn: “Cục Thống kê, xử lý bởi Vietnam in Data (vietnamindata.com)” kèm liên kết.

## Giấy phép / License

Phần tổng hợp, quy đổi địa giới, mã cờ và từ điển: **CC BY 4.0** — tự do dùng lại, kể cả thương mại, khi ghi nguồn.
Số liệu gốc là thông tin thống kê nhà nước của Cục Thống kê; khi dùng phải trích dẫn nguồn. Xem `LICENSE.md`.

## Cập nhật / Updates

Bản này tạo ngày 2026-11-13. Số mới nhất luôn ở <https://vietnamindata.com>; bộ dữ liệu được đăng lại khi Cục Thống kê công bố số mới.
Mã nguồn kho này: <https://github.com/pkvip9999/vietnam-34-provinces-data>.
