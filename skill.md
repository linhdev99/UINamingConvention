---
name: ui-asset-naming
description: Đặt tên file tài nguyên UI (sprite, icon, popup, button, frame, background...) theo quy ước chuẩn của dự án. Dùng khi tạo, đổi tên, hoặc kiểm tra tên file asset UI.
---

# Quy tắc đặt tên tài nguyên UI

## Cấu trúc tổng quát

```
[9slice?][type][feature?][color]_[size?]_[index?]
```

Dấu `?` nghĩa là phần không bắt buộc.

## Mô tả các phần

| Thành phần | Bắt buộc | Mô tả |
|---|---|---|
| `9slice` | Không | Nếu sprite dùng 9-slice, thêm tiền tố `9slice` |
| `type` | Có | Kiểu tài nguyên: `btn`, `icon`, `frame`, `bg`, `avatar`, `popup`, `title`, ... |
| `feature` | Không | Tên tính năng sử dụng riêng biệt: `Native`, `Shop`, `Setting`, ... |
| `color` | Có | Màu chính: `Gray`, `Blue`, `Red`, ... |
| `size` | Không | Kích cỡ: `Big`, `Small`, ... |
| `index` | Không | Phiên bản thứ tự: `1`, `2`, ... |

## Quy tắc viết hoa

- Chữ cái đầu của tên file luôn viết thường.
- Nếu sử dụng 9-slice, tên file phải bắt đầu bằng `9slice`, ví dụ: `9sliceFrameBlue_1` hoặc `9slice_frameBlue_1`.
- Giữ nhất quán quy tắc này trong toàn bộ dự án để dễ đọc và quản lý tài nguyên.
- Chỉ viết hoa chữ cái đầu của các phần bắt buộc tiếp theo (`type`, `feature`, `color`...), giữ nhất quán kiểu chữ trong toàn bộ dự án.

## Lưu ý quan trọng

- Không sử dụng tiếng Việt hoặc ký tự đặc biệt trong tên file.
- Nếu tài nguyên dùng cho nhiều tính năng, bỏ qua phần `feature` để dùng chung.
- Với tài nguyên có nhiều biến thể màu hoặc kích thước, luôn bổ sung `color` và `size` để dễ phân biệt.
- Đặt tên ngắn gọn, dễ hiểu, ưu tiên mô tả chức năng chính của tài nguyên.
- Nếu có nhiều phiên bản, luôn thêm `index` để tránh ghi đè file.
- Dùng dấu gạch dưới `_` để phân tách các phần, không dùng dấu cách hoặc dấu gạch ngang `-`.
- Về `9slice`: chỉ dùng dạng **tiền tố** (`9slice_frameBlue_1` hoặc `9sliceFrameBlue_1`), tuyệt đối không dùng hậu tố. Không pha trộn hai cách viết trong cùng một project.

## Ví dụ đặt tên

| Tên File | Giải thích |
|---|---|
| `9slice_btnShopGray_Big_3` | Button xám, to, dùng trong Shop, có 9-slice, phiên bản thứ 3 |
| `9sliceFrameProfileBlue_1` | Frame hồ sơ, màu xanh, có 9-slice, phiên bản 1 |
| `btnGray` | Nút màu xám, dùng chung |
| `btnLoginBlue_Big` | Nút màu xanh, to, dùng riêng cho tính năng Login |
| `btnShopRed_Small_2` | Nút đỏ, nhỏ, phiên bản thứ 2 dùng riêng trong Shop |
| `bgNative_Big` | Background to dùng riêng trong UI Native |
| `iconAvatarGray_Small` | Icon avatar màu xám, kích thước nhỏ |
| `avatarFriendRed_Small_2` | Avatar bạn bè, màu đỏ, nhỏ, phiên bản thứ 2 |
| `frameAchievementGold_Wide_2` | Frame thành tựu, màu vàng, rộng, bản 2 |
| `popupSetting` | Popup dùng riêng cho UI cài đặt |
| `titleMatchmakingBlue_Big` | Tiêu đề trong UI matchmaking, màu xanh, to |

### Ví dụ chức năng phụ (hậu tố mô tả vai trò riêng trong 1 feature)

| Tên File | Chức năng phụ | Giải thích |
|---|---|---|
| `popupBg` | Bg | Hình nền của popup, phân biệt với popup chính |
| `iconAvatarGray` | Avatar | Icon đại diện người dùng |
| `frameProfileBlue` | Profile | Frame dành riêng cho giao diện hồ sơ |

## Gợi ý tên feature (chung)

`Setting`, `Shop`, `Tutorial`, `Quest`, `Gacha`, `DailyReward`, `Matchmaking`, `Upgrade`, `Login`, `InviteFriend`, `Profile`, `Event`, `Victory`, `Defeat`, `Achievement`, `Background`, `GachaTicket`, `GiftBox`, `Card`, `Result`, `MainUI`, `Support`, `SpecialEvent`, `Notification`, `LoginReward`, `Leaderboard`, `Mailbox`, `Redeem`, `TopUp`, `LuckySpin`, `Guide`

## Gợi ý tên feature cho game chiến thuật (Strategy)

`Character`, `Formation`, `Skill`, `Equipment`, `Campaign`, `Map`, `Army`, `Faction`, `UpgradeCharacter`, `ManageFormation`, `BaseBuilding`, `ResourceCollection`, `TechResearch`, `Defense`, `Attack`, `Occupation`, `Trade`, `TroopManagement`, `Arena`, `SideQuest`, `Alliance`, `BattleStats`, `Ranking`, `Training`, `TerritoryExpansion`, `Strategy`, `ResourceManagement`, `Exploration`, `Diplomacy`

## Gợi ý tên feature cho game casual

`Home`, `QuickPlay`, `DailyQuest`, `LuckyWheel`, `Collection`, `Achievement`, `ItemShop`, `LoginReward`, `Leaderboard`, `SpecialEvent`, `Mailbox`, `Notification`, `Support`, `Redeem`, `Guide`, `InviteFriend`, `OfferPack`, `TopUp`, `Challenge`, `MiniGame`, `FreeGift`, `Spin`, `Unlock`, `Upgrade`, `ChangeAvatar`, `Setting`

## Gợi ý tên màu sắc

`Gray`, `Blue`, `Red`, `Yellow`, `Green`, `Purple`, `Orange`, `Gold`, `Black`, `White`, `Brown`, `Pink`, `Cyan`, `Teal`, `Silver`, `Copper`

## Gợi ý tên kích thước

`Big`, `Small`, `Tiny`, `Wide`, `Tall`, `Long`, `Short`

## Định dạng nâng cao (snake_case, tùy chọn nếu cả team thống nhất)

```
[type]_[feature?]_[color]_[size?]_[index?]_[9slice?]
```

Ví dụ: `btn_shop_gray_big_2_9slice`, `bg_dailyreward_gray_9slice`, `frame_profile_blue_9slice`

## Checklist khi đặt tên 1 file asset UI

1. Xác định `type` (bắt buộc).
2. Có dùng chung nhiều feature không? Nếu không, thêm `feature`.
3. Xác định `color` chính (bắt buộc).
4. Có nhiều biến thể kích thước không? Nếu có, thêm `size`.
5. Có nhiều phiên bản/biến thể không? Nếu có, thêm `index`.
6. Có dùng 9-slice không? Nếu có, thêm tiền tố `9slice` (không dùng hậu tố).
7. Ghép lại theo đúng thứ tự, phân tách bằng `_`, không dấu, không ký tự đặc biệt.
