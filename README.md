## Quy tắc đặt tên tài nguyên UI

### Cấu trúc tổng quát

```
[9slice?][type][feature?][color]_[size?]_[index?]
```

### Mô tả các phần:

| Thành phần | Bắt buộc | Mô tả                                                                                                                                       |
| ---------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `9slice`   | ❌       | Nếu sprite dùng 9-slice, thêm tiền tố `9slice` hoặc hậu tố `_9slice`                                                                        |
| `type`     | ✅       | Kiểu tài nguyên: `btn`, `icon`, `frame`, `bg`, `avatar`, `popup`, `title`, ... Có thể là cụm từ ghép như `popupBg` nếu cần rõ chức năng phụ |
| `feature`  | ❌       | Tên tính năng sử dụng riêng biệt: `Native`, `Shop`, `Setting`, ... Nếu dùng chung giữa nhiều UI thì bỏ qua                                  |
| `color`    | ✅       | Màu chính: `Gray`, `Blue`, `Red`, `Yellow`, ...                                                                                             |
| `size`     | ❌       | Kích cỡ: `Big`, `Small`, `Tiny`, `Wide`, ...                                                                                                |
| `index`    | ❌       | Phiên bản thứ tự: `1`, `2`, `3`, ...                                                                                                        |

### Quy tắc viết hoa

- Chữ cái đầu của tên file luôn viết thường.
- Nếu sử dụng 9-slice, tên file phải bắt đầu bằng `9slice`, ví dụ: `9sliceFrameBlue_1` hoặc `9slice_frameBlue_1`, sau đó đến các thành phần còn lại (`type`, `feature`, `color`, `size`, ...).
- Giữ nhất quán quy tắc này trong toàn bộ dự án để dễ đọc và quản lý tài nguyên.

> ⚠️ **Lưu ý quan trọng:**
>
> - Không sử dụng tiếng Việt hoặc ký tự đặc biệt trong tên file.
> - Chỉ viết hoa chữ cái đầu của các phần bắt buộc, giữ nhất quán kiểu chữ trong toàn bộ dự án.
> - Nếu tài nguyên dùng cho nhiều tính năng, hãy bỏ qua phần `feature` để dùng chung.
> - Với tài nguyên có nhiều biến thể màu hoặc kích thước, luôn bổ sung phần `color` và `size` để dễ phân biệt.
> - Đặt tên ngắn gọn, dễ hiểu, ưu tiên mô tả chức năng chính của tài nguyên.
> - Nếu có nhiều phiên bản, luôn thêm phần `index` để tránh ghi đè file.
> - Sử dụng dấu gạch dưới `_` để phân tách các phần, không dùng dấu cách hoặc dấu gạch ngang `-`.

> 💡 **Lưu ý về cách viết `9slice`:**
>
> - Chỉ **dùng tiền tố** `9slice` (ví dụ: `9slice_frameBlue_1` hoặc `9sliceFrameBlue_1`) và **tuyệt đối không dùng hậu tố** như `frameBlue_1_9slice`.
> - 🚫 Không pha trộn hai cách viết trong cùng một project để tránh nhầm lẫn và dễ quản lý tài nguyên.

## 🧪 Ví Dụ Đặt Tên

| Tên File                          | Giải Thích                                                   |
| --------------------------------- | ------------------------------------------------------------ |
| `9slice_btnShopGray_Big_3`        | Button xám, to, dùng trong Shop, có 9-slice, phiên bản thứ 3 |
| `9sliceBtnShopGray_Big_3`         | Button xám, to, dùng trong Shop, có 9-slice, phiên bản thứ 3 |
| `9slice_frameProfileBlue_1`       | Frame hồ sơ, màu xanh, có 9-slice, phiên bản 1               |
| `9sliceFrameProfileBlue_1`        | Frame hồ sơ, màu xanh, có 9-slice, phiên bản 1               |
| `9slice_popupUpgradeBlue_Big`     | Popup nâng cấp, màu xanh, to, có 9-slice                     |
| `9slicePopupUpgradeBlue_Big`      | Popup nâng cấp, màu xanh, to, có 9-slice                     |
| `9sliceBgDailyRewardGray`         | Background thưởng ngày, màu xám, có 9-slice                  |
| `9sliceFrameProfileBlue`          | Frame giao diện Profile, màu xanh, dùng 9-slice              |
| `btnGray`                         | Nút màu xám, dùng chung                                      |
| `btnLoginBlue_Big`                | Nút màu xanh, to, dùng riêng cho tính năng Login             |
| `btnShopRed_Small_2`              | Nút đỏ, nhỏ, phiên bản thứ 2 dùng riêng trong Shop           |
| `btnTutorialGreen_Tiny`           | Button xanh lá nhỏ dành riêng cho Tutorial                   |
| `btnInviteFriendPurple_Small`     | Nút mời bạn, màu tím, nhỏ                                    |
| `btnDailyRewardOrange_Tall_1`     | Nút thưởng ngày, màu cam, cao, bản 1                         |
| `bgNative_Big`                    | Background to dùng riêng trong UI Native                     |
| `bg_Big`                          | Background to, dùng chung                                    |
| `iconAvatarGray_Small`            | Icon avatar màu xám, kích thước nhỏ                          |
| `iconRewardYellow_1`              | Icon phần thưởng màu vàng, biến thể thứ 1                    |
| `iconCurrencyGold_Small`          | Icon tiền vàng, nhỏ                                          |
| `iconLevelUpBlue_Small`           | Icon lên cấp, màu xanh, nhỏ                                  |
| `iconMissionYellow_2`             | Icon nhiệm vụ, màu vàng, bản số 2                            |
| `iconGachaTicketRed_Tiny`         | Icon vé gacha, màu đỏ, kích thước nhỏ                        |
| `iconQuestStarYellow_Small_2`     | Icon sao nhiệm vụ, vàng, nhỏ, bản 2                          |
| `avatarFriendRed_Small_2`         | Avatar bạn bè, màu đỏ, nhỏ, phiên bản thứ 2                  |
| `frameAchievementGold_Wide_2`     | Frame thành tựu, màu vàng, rộng, bản 2                       |
| `frameEventRed_Big_1`             | Frame dùng trong sự kiện, đỏ, to, bản 1                      |
| `popupSetting`                    | Popup dùng riêng cho UI cài đặt                              |
| `popupWarning_Red`                | Popup cảnh báo, màu đỏ                                       |
| `popupBackgroundGray_1`           | Hình nền của popup, màu xám, phiên bản 1                     |
| `titleMatchmakingBlue_Big`        | Tiêu đề trong UI matchmaking, màu xanh, to                   |
| `titleEventHalloweenPurple_Big_1` | Tiêu đề sự kiện Halloween, màu tím, to, bản 1                |

### Ví dụ về chức năng phụ

| Tên File           | Chức năng phụ | Giải Thích                                     |
| ------------------ | ------------- | ---------------------------------------------- |
| `popupBg`          | `Bg`          | Hình nền của popup, phân biệt với popup chính  |
| `btnShopRed_Small` | `Shop`        | Nút dùng riêng cho cửa hàng                    |
| `iconAvatarGray`   | `Avatar`      | Icon đại diện người dùng                       |
| `frameProfileBlue` | `Profile`     | Frame dành riêng cho giao diện hồ sơ           |
| `titleMatchmaking` | `Matchmaking` | Tiêu đề dùng riêng cho UI ghép trận            |
| `iconQuestStar`    | `QuestStar`   | Icon sao nhiệm vụ, phân biệt với icon nhiệm vụ |

### Gợi ý tên feature

| Feature UI             | Gợi ý đặt tên feature |
| ---------------------- | --------------------- |
| Cài đặt                | `Setting`             |
| Cửa hàng               | `Shop`                |
| Hướng dẫn              | `Tutorial`            |
| Nhiệm vụ               | `Quest`               |
| Gacha                  | `Gacha`               |
| Thưởng ngày            | `DailyReward`         |
| Matchmaking            | `Matchmaking`         |
| Nâng cấp               | `Upgrade`             |
| Đăng nhập              | `Login`               |
| Mời bạn                | `InviteFriend`        |
| Hồ sơ người chơi       | `Profile`             |
| Sự kiện                | `Event`               |
| Chiến thắng            | `Victory`             |
| Thất bại               | `Defeat`              |
| Thành tựu              | `Achievement`         |
| Giao diện nền popup    | `Background`          |
| Vé gacha               | `GachaTicket`         |
| Hộp quà                | `GiftBox`             |
| Thẻ bài                | `Card`                |
| Màn hình kết thúc trận | `Result`              |
| Giao diện chính        | `MainUI`              |
| Hỗ trợ khách hàng      | `Support`             |
| Sự kiện đặc biệt       | `SpecialEvent`        |
| Thông báo              | `Notification`        |
| Quà đăng nhập          | `LoginReward`         |
| Bảng xếp hạng          | `Leaderboard`         |
| Hòm thư                | `Mailbox`             |
| Đổi thưởng             | `Redeem`              |
| Nạp tiền               | `TopUp`               |
| Quay số may mắn        | `LuckySpin`           |
| Hướng dẫn chơi         | `Guide`               |

### Gợi ý tên feature cho game chiến thuật (Strategy)

| Feature UI           | Gợi ý đặt tên feature |
| -------------------- | --------------------- |
| Nhân vật             | `Character`           |
| Đội hình             | `Formation`           |
| Kỹ năng              | `Skill`               |
| Trang bị             | `Equipment`           |
| Chiến dịch           | `Campaign`            |
| Bản đồ               | `Map`                 |
| Quân đội             | `Army`                |
| Lực lượng            | `Faction`             |
| Nâng cấp nhân vật    | `UpgradeCharacter`    |
| Quản lý đội hình     | `ManageFormation`     |
| Xây dựng căn cứ      | `BaseBuilding`        |
| Thu thập tài nguyên  | `ResourceCollection`  |
| Nghiên cứu công nghệ | `TechResearch`        |
| Phòng thủ            | `Defense`             |
| Tấn công             | `Attack`              |
| Chiếm đóng           | `Occupation`          |
| Giao dịch            | `Trade`               |
| Quản lý quân lính    | `TroopManagement`     |
| Sự kiện đặc biệt     | `SpecialEvent`        |
| Đấu trường           | `Arena`               |
| Nhiệm vụ phụ         | `SideQuest`           |
| Hợp tác đồng minh    | `Alliance`            |
| Thống kê trận đấu    | `BattleStats`         |
| Xếp hạng             | `Ranking`             |
| Huấn luyện           | `Training`            |
| Mở rộng lãnh thổ     | `TerritoryExpansion`  |
| Chiến thuật          | `Strategy`            |
| Quản lý tài nguyên   | `ResourceManagement`  |
| Thám hiểm            | `Exploration`         |
| Đàm phán             | `Diplomacy`           |

### Gợi ý tên feature cho game casual

| Feature UI            | Gợi ý đặt tên feature |
| --------------------- | --------------------- |
| Trang chủ             | `Home`                |
| Chơi nhanh            | `QuickPlay`           |
| Nhiệm vụ ngày         | `DailyQuest`          |
| Vòng quay may mắn     | `LuckyWheel`          |
| Sưu tập               | `Collection`          |
| Thành tích            | `Achievement`         |
| Cửa hàng vật phẩm     | `ItemShop`            |
| Quà đăng nhập         | `LoginReward`         |
| Bảng xếp hạng         | `Leaderboard`         |
| Sự kiện đặc biệt      | `SpecialEvent`        |
| Hòm thư               | `Mailbox`             |
| Thông báo             | `Notification`        |
| Hỗ trợ                | `Support`             |
| Đổi thưởng            | `Redeem`              |
| Hướng dẫn chơi        | `Guide`               |
| Mời bạn               | `InviteFriend`        |
| Gói ưu đãi            | `OfferPack`           |
| Nạp tiền              | `TopUp`               |
| Thử thách             | `Challenge`           |
| Mini game             | `MiniGame`            |
| Quà miễn phí          | `FreeGift`            |
| Quay thưởng           | `Spin`                |
| Mở khóa               | `Unlock`              |
| Nâng cấp              | `Upgrade`             |
| Đổi avatar            | `ChangeAvatar`        |
| Cài đặt               | `Setting`             |

### Gợi ý tên màu sắc

| Màu sắc    | Tên đặt màu | Hiển thị màu                                                                                                |
| ---------- | ----------- | ----------------------------------------------------------------------------------------------------------- |
| Xám        | `Gray`      | <span style="display:inline-block;width:24px;height:16px;background:#808080;border:1px solid #ccc;"></span> |
| Xanh dương | `Blue`      | <span style="display:inline-block;width:24px;height:16px;background:#2196F3;border:1px solid #ccc;"></span> |
| Đỏ         | `Red`       | <span style="display:inline-block;width:24px;height:16px;background:#F44336;border:1px solid #ccc;"></span> |
| Vàng       | `Yellow`    | <span style="display:inline-block;width:24px;height:16px;background:#FFEB3B;border:1px solid #ccc;"></span> |
| Xanh lá    | `Green`     | <span style="display:inline-block;width:24px;height:16px;background:#4CAF50;border:1px solid #ccc;"></span> |
| Tím        | `Purple`    | <span style="display:inline-block;width:24px;height:16px;background:#9C27B0;border:1px solid #ccc;"></span> |
| Cam        | `Orange`    | <span style="display:inline-block;width:24px;height:16px;background:#FF9800;border:1px solid #ccc;"></span> |
| Vàng kim   | `Gold`      | <span style="display:inline-block;width:24px;height:16px;background:#FFD700;border:1px solid #ccc;"></span> |
| Đen        | `Black`     | <span style="display:inline-block;width:24px;height:16px;background:#222;border:1px solid #ccc;"></span>    |
| Trắng      | `White`     | <span style="display:inline-block;width:24px;height:16px;background:#fff;border:1px solid #ccc;"></span>    |
| Nâu        | `Brown`     | <span style="display:inline-block;width:24px;height:16px;background:#795548;border:1px solid #ccc;"></span> |
| Hồng       | `Pink`      | <span style="display:inline-block;width:24px;height:16px;background:#E91E63;border:1px solid #ccc;"></span> |
| Xanh ngọc  | `Cyan`      | <span style="display:inline-block;width:24px;height:16px;background:#00BCD4;border:1px solid #ccc;"></span> |
| Xanh biển  | `Teal`      | <span style="display:inline-block;width:24px;height:16px;background:#009688;border:1px solid #ccc;"></span> |
| Bạc        | `Silver`    | <span style="display:inline-block;width:24px;height:16px;background:#C0C0C0;border:1px solid #ccc;"></span> |
| Đồng       | `Copper`    | <span style="display:inline-block;width:24px;height:16px;background:#B87333;border:1px solid #ccc;"></span> |

### Gợi ý tên kích thước

| Kích thước | Tên đặt kích thước |
| ---------- | ------------------ |
| To         | `Big`              |
| Nhỏ        | `Small`            |
| Rất nhỏ    | `Tiny`             |
| Rộng       | `Wide`             |
| Cao        | `Tall`             |
| Dài        | `Long`             |
| Ngắn       | `Short`            |

### Nếu đã dùng quy tắc ở trên thì không cần đọc gợi ý nâng cao, lưu ý chỉ chọn 1 cho nhất quán

### Gợi ý nâng cao (định dạng tối ưu nên dùng nếu nhất quán toàn bộ team):

```
[type]_[feature?]_[color]_[size?]_[index?]_[9slice?]
```

Ví dụ: `btn_shop_gray_big_2_9slice`

### Ví dụ nâng cao

| Tên File                             | Giải Thích                                                   |
| ------------------------------------ | ------------------------------------------------------------ |
| `btn_shop_gray_big_2_9slice`         | Button dùng trong Shop, màu xám, to, phiên bản 2, có 9-slice |
| `icon_profile_blue_small`            | Icon hồ sơ người chơi, màu xanh dương, nhỏ                   |
| `bg_dailyreward_gray_9slice`         | Background thưởng ngày, màu xám, có 9-slice                  |
| `frame_event_red_big_1`              | Frame sự kiện, màu đỏ, to, bản 1                             |
| `popup_setting_red`                  | Popup cài đặt, màu đỏ                                        |
| `title_matchmaking_blue_big`         | Tiêu đề matchmaking, màu xanh dương, to                      |
| `icon_gacha_ticket_red_tiny`         | Icon vé gacha, màu đỏ, rất nhỏ                               |
| `btn_tutorial_green_tiny`            | Button hướng dẫn, màu xanh lá, rất nhỏ                       |
| `avatar_friend_red_small_2`          | Avatar bạn bè, màu đỏ, nhỏ, phiên bản 2                      |
| `icon_quest_star_yellow_small_2`     | Icon sao nhiệm vụ, màu vàng, nhỏ, bản 2                      |
| `frame_achievement_gold_wide_2`      | Frame thành tựu, màu vàng kim, rộng, bản 2                   |
| `btn_dailyreward_orange_tall_1`      | Nút thưởng ngày, màu cam, cao, bản 1                         |
| `bg_victory_green_big`               | Background chiến thắng, màu xanh lá, to                      |
| `icon_mission_yellow_2`              | Icon nhiệm vụ, màu vàng, bản số 2                            |
| `popup_background_gray_1`            | Hình nền popup, màu xám, phiên bản 1                         |
| `icon_currency_gold_small`           | Icon tiền vàng, nhỏ                                          |
| `frame_profile_blue_9slice`          | Frame hồ sơ, màu xanh dương, có 9-slice                      |
| `btn_invitefriend_purple_small`      | Nút mời bạn, màu tím, nhỏ                                    |
| `icon_levelup_blue_small`            | Icon lên cấp, màu xanh dương, nhỏ                            |
| `bg_native_big`                      | Background dùng riêng cho UI Native, to                      |
| `icon_giftbox_pink_tiny`             | Icon hộp quà, màu hồng, rất nhỏ                              |
| `card_result_brown_long`             | Thẻ bài kết thúc trận, màu nâu, dài                          |
| `popup_defeat_black`                 | Popup thất bại, màu đen                                      |
| `title_event_halloween_purple_big_1` | Tiêu đề sự kiện Halloween, màu tím, to, bản 1                |

---

> _Được viết bởi Istaroth [PL], mong nhận được đóng góp thêm để hoàn thiện quy tắc này. Nếu có ý kiến hoặc bổ sung, vui lòng gửi phản hồi qua email hoặc mở issue trên repository._
