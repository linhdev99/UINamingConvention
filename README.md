## Quy tắc đặt tên tài nguyên UI

### Cấu trúc tổng quát
```
[9scale?][type][feature?][color]_[size?]_[index?]
```

### Mô tả các phần:
| Thành phần     | Bắt buộc | Mô tả |
|----------------|----------|-------|
| `9scale`       | ❌       | Nếu sprite dùng 9-slice, thêm tiền tố `9scale` hoặc hậu tố `_9scale` |
| `type`         | ✅       | Kiểu tài nguyên: `btn`, `icon`, `frame`, `bg`, `avatar`, `popup`, `title`, ... Có thể là cụm từ ghép như `popupBackground` nếu cần rõ chức năng phụ |
| `feature`      | ❌       | Tên tính năng sử dụng riêng biệt: `Native`, `Shop`, `Setting`, ... Nếu dùng chung giữa nhiều UI thì bỏ qua |
| `color`        | ✅       | Màu chính: `Gray`, `Blue`, `Red`, `Yellow`, ... |
| `size`         | ❌       | Kích cỡ: `Big`, `Small`, `Tiny`, `Wide`, ... |
| `index`        | ❌       | Phiên bản thứ tự: `1`, `2`, `3`, ... |

### Ví dụ đặt tên
| Tên File                            | Giải Thích                                                                 |
|-------------------------------------|----------------------------------------------------------------------------|
| `btnGray`                           | Nút màu xám, dùng chung                                                   |
| `btnLoginBlue_Big`                 | Nút màu xanh, to, dùng riêng cho tính năng Login                         |
| `btnShopRed_Small_2`               | Nút đỏ, nhỏ, phiên bản thứ 2 dùng riêng trong Shop                        |
| `bgNative_Big`                      | Background to dùng riêng trong UI Native                                  |
| `bg_Big`                            | Background to, dùng chung                                                 |
| `iconAvatarGray_Small`             | Icon avatar màu xám, kích thước nhỏ                                       |
| `iconRewardYellow_1`               | Icon phần thưởng màu vàng, biến thể thứ 1                                 |
| `frameProfileBlue_9scale`          | Frame giao diện Profile, màu xanh, dùng 9-slice                           |
| `avatarFriendRed_Small_2`          | Avatar bạn bè, màu đỏ, nhỏ, phiên bản thứ 2                               |
| `popupSetting`                      | Popup dùng riêng cho UI cài đặt                                           |
| `popupWarning_Red`                 | Popup cảnh báo, màu đỏ                                                    |
| `titleMatchmakingBlue_Big`         | Tiêu đề trong UI matchmaking, màu xanh, to                               |
| `9scale_btnShopGray_Big_3`         | Button xám, to, dùng trong Shop, 9scale, phiên bản thứ 3 (nếu giữ `9scale` đầu) |
| `btnTutorialGreen_Tiny`            | Button xanh lá nhỏ dành riêng cho Tutorial                                |
| `iconCurrencyGold_Small`           | Icon tiền vàng, nhỏ                                                        |
| `bgDailyRewardGray_9scale`         | Background dùng trong Daily Reward, màu xám, có 9-slice                   |
| `iconLevelUpBlue_Small`            | Icon lên cấp, màu xanh, nhỏ                                               |
| `frameEventRed_Big_1`              | Frame dùng trong sự kiện, đỏ, to, bản 1                                   |
| `btnInviteFriendPurple_Small`      | Nút mời bạn, màu tím, nhỏ                                                 |
| `bgVictoryGreen_Big`               | Background chiến thắng, màu xanh lá, to                                   |
| `iconMissionYellow_2`              | Icon nhiệm vụ, màu vàng, bản số 2                                         |
| `popupBackgroundGray_1`            | Hình nền của popup, màu xám, phiên bản 1                                  |

### Gợi ý tên feature
| Feature UI         | Gợi ý đặt tên feature |
|--------------------|------------------------|
| Cài đặt            | `Setting`              |
| Cửa hàng           | `Shop`                 |
| Hướng dẫn          | `Tutorial`             |
| Nhiệm vụ           | `Quest`                |
| Gacha              | `Gacha`                |
| Thưởng ngày        | `DailyReward`          |
| Matchmaking        | `Matchmaking`          |
| Nâng cấp           | `Upgrade`              |
| Đăng nhập          | `Login`                |
| Mời bạn            | `InviteFriend`         |
| Hồ sơ người chơi   | `Profile`              |
| Sự kiện            | `Event`                |
| Chiến thắng        | `Victory`              |
| Thất bại           | `Defeat`               |
| Thành tựu          | `Achievement`          |
| Giao diện nền popup| `Background`           |

### Gợi ý nâng cao (định dạng tối ưu nên dùng nếu nhất quán toàn bộ team):
```
[type]_[feature?]_[color]_[size?]_[index?]_[9scale?]
```
Ví dụ: `btn_shop_gray_big_2_9scale`

