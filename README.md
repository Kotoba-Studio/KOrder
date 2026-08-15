# 📦 KOrder

[![Minecraft Version](https://img.shields.io/badge/Minecraft-1.21%2B-brightgreen.svg)](https://papermc.io)
[![Platform](https://img.shields.io/badge/Platform-Paper%20%7C%20Folia-blue.svg)](https://papermc.io)
[![Folia Support](https://img.shields.io/badge/Folia-Supported-success.svg)](https://papermc.io/software/folia)
[![Build](https://img.shields.io/badge/Build-R02--v2-8A5CF6.svg)](#)

**KOrder** là hệ thống **Buy Order Marketplace** dành cho EcoSMP, cho phép người chơi đăng đơn mua vật phẩm với số lượng và mức giá mong muốn để những người chơi khác giao hàng trực tiếp.

Tiền của đơn được giữ an toàn trong quá trình giao dịch, người bán nhận thanh toán khi giao thành công và vật phẩm của người mua được chuyển vào kho nhận hàng riêng.

---

## ✨ Tính năng

- **Buy Order Marketplace** — tạo đơn mua theo vật phẩm, số lượng và giá mỗi món.
- **Partial Delivery** — nhiều người chơi có thể giao từng phần cho cùng một đơn cho tới khi hoàn tất.
- **Safe Payment Flow** — giữ tiền khi tạo đơn, thanh toán khi giao thành công và hoàn tiền phần còn lại khi huỷ hoặc hết hạn.
- **Exact Item Matching** — hỗ trợ tạo đơn từ vật phẩm đang cầm và kiểm tra chính xác item meta khi giao hàng.
- **Delivery Stash** — vật phẩm đã giao được giữ trong kho nhận hàng nếu túi đồ của người mua không đủ chỗ.
- **Search, Filter & Sort** — tìm theo người chơi hoặc vật phẩm, lọc category và sắp xếp đơn theo nhiều tiêu chí.
- **Modern GUI** — 3 preset `modern`, `king` và `custom`, hỗ trợ tùy chỉnh layout và button.
- **Java & Bedrock UI** — hỗ trợ Dialog/Anvil fallback cho Java và Bedrock Form khi dùng Geyser/Floodgate.
- **Multi-Economy** — hỗ trợ VaultUnlocked, Vault, PlayerPoints và các economy provider tương thích.
- **Multi-Language** — tích hợp sẵn tiếng Việt, Anh, Tây Ban Nha, Bồ Đào Nha và Đức.
- **PlaceholderAPI & Discord Webhook** — placeholder có cache bất đồng bộ và webhook cho các sự kiện giao dịch quan trọng.
- **Folia Ready** — scheduler và xử lý I/O được thiết kế để hoạt động an toàn trên Paper/Folia hiện đại.

---

## 📜 Lệnh chính

| Lệnh | Mô tả |
| :--- | :--- |
| `/korder` | Mở KOrder Marketplace |
| `/korder browse` | Xem các đơn mua đang hoạt động |
| `/korder search <query>` | Tìm theo người chơi hoặc vật phẩm |
| `/korder create` | Tạo đơn mua mới |
| `/korder mine` | Xem các đơn của bạn |
| `/korder stash` | Mở kho nhận hàng |
| `/korder deliver <id> <amount>` | Giao vật phẩm cho một đơn |
| `/korder add <id> <amount>` | Tăng số lượng của đơn đang mở |
| `/korder reload` | Reload cấu hình và ngôn ngữ |
| `/korder admin` | Mở các công cụ quản trị |

Aliases của lệnh chính: `/order`, `/orders`, `/donhang`.

---

## 🔗 Economy & Tích hợp

KOrder tự động kết nối với các plugin tương thích khi chúng có mặt trên server:

- **VaultUnlocked v2**
- **Vault**
- **PlayerPoints**
- **CoinsEngine**
- **ExcellentEconomy**
- **LuckPerms**
- **PlaceholderAPI**
- **Geyser / Floodgate**
- **ViaVersion**

Ở chế độ `auto`, KOrder ưu tiên **VaultUnlocked**, sau đó **Vault**, rồi **PlayerPoints** trực tiếp.

---

## 🛡️ Giao dịch an toàn

KOrder có nhiều lớp bảo vệ dành cho marketplace:

- Khóa thao tác ngắn để hạn chế double-click và giao dịch trùng.
- Kiểm tra item giao có khớp chính xác với đơn.
- Chặn item overstack bất thường theo cấu hình.
- Kho nhận hàng giữ vật phẩm khi inventory không còn chỗ.
- SQLite sử dụng WAL và cơ chế ghi tuần tự để giảm rủi ro dữ liệu.
- Audit transaction và công cụ admin để kiểm tra giao dịch cần xử lý.

---

## 📥 Cài đặt

1. Thả `KOrder-R02-v2.jar` vào thư mục `plugins/`.
2. Cài một economy provider phù hợp, ví dụ **Vault** hoặc **VaultUnlocked**.
3. Khởi động server một lần để KOrder tạo cấu hình mặc định.
4. Chỉnh `config.yml` và preset trong `plugins/KOrder/settings/` theo nhu cầu.
5. Restart server hoặc sử dụng `/korder reload` với các phần hỗ trợ reload.

---

## 👥 Hỗ trợ

Phát triển bởi **Kotoba Studio / K-Studio**.

- Discord: `https://discord.gg/x9ScDT7fCV`
