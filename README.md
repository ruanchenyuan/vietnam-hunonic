# Hunonic Smart Home – Home Assistant Integration

Custom Home Assistant integration for Hunonic smart-home devices.

Integration này kết nối Home Assistant với hệ thống Hunonic thông qua API và MQTT, cho phép theo dõi và điều khiển các thiết bị Hunonic trực tiếp từ Home Assistant.

## Tính năng

- Kết nối tài khoản Hunonic với Home Assistant.
- Tự động lấy danh sách thiết bị từ tài khoản.
- Nhận trạng thái realtime thông qua MQTT.
- Điều khiển thiết bị thông qua MQTT.
- Hỗ trợ nhiều nhóm `root_type` của Hunonic.
- Tự phát hiện thiết bị mới.
- Hỗ trợ các platform tùy theo loại thiết bị:
  - Sensor
  - Switch
  - Cover
  - Light
  - Fan
  - Select
- Hỗ trợ các dữ liệu đo điện năng khi thiết bị cung cấp:
  - Công suất
  - Điện áp
  - Dòng điện
  - Điện năng
  - Chỉ số công tơ tích lũy
  - Nhiệt độ
- MQTT refresh tự động cho các thiết bị đo điện phù hợp.
- Device Registry sử dụng định danh thiết bị riêng, giúp các thiết bị có cùng tên nhưng khác thiết bị vật lý không bị gộp thành một Device.

## Cài đặt bằng HACS

### 1. Mở HACS

Trong Home Assistant:

**HACS → Integrations**

### 2. Thêm Custom Repository

Chọn:

**⋮ → Custom repositories**

Thêm:

```text
ruanchenyuan/vietnam-hunonic
```

Chọn loại:

```text
Integration
```

Sau đó chọn **Add**.

### 3. Cài đặt

Tìm:

**Hunonic**

Chọn **Download**.

Sau khi cài đặt, khởi động lại Home Assistant.

### 4. Thêm Integration

Vào:

**Settings → Devices & services → Add Integration**

Tìm:

**Hunonic**

Sau đó đăng nhập bằng tài khoản Hunonic dành cho Home Assistant.

## Lưu ý về tài khoản Hunonic

Nếu tài khoản Hunonic đang được sử dụng thường xuyên trên ứng dụng chính và gặp giới hạn phiên đăng nhập, nên sử dụng một tài khoản Hunonic riêng cho Home Assistant và chia sẻ các nhà/thiết bị cần thiết sang tài khoản đó.

Việc chia sẻ nhà và thiết bị phải được thực hiện từ hệ thống Hunonic trước khi Home Assistant có thể nhìn thấy các thiết bị được chia sẻ.

## Cấu trúc repository

```text
vietnam-hunonic/
├── custom_components/
│   └── hunonic/
├── docs/
├── assets/
├── hunonic/
├── hacs.json
├── README.md
└── LICENSE
```

## Tài liệu

- [Mobile API](docs/mobile-api.md)
- [MQTT Control](docs/mqtt-control.md)
- [Web API](docs/web-api.md)
- [Local Control](docs/local-control.md)
- [Reverse Engineering](docs/reverse-engineering.md)
- [API Reference](docs/api.md)

## Version

Current release:

**1.15.0**

---

## ☕ Ủng hộ tác giả

Nếu bạn cảm thấy hữu ích, hãy ủng hộ tôi một cốc coffee để tôi có thể thêm ý tưởng phát triển thêm những dự án về sau.

**Địa chỉ ủng hộ USDT (TRC20):**

`TUt6c19fkDfrpZHhVaENrdH5UdtUcFMmwP`

<p align="center">
  <img src="assets/donate-qr.png" alt="Địa chỉ ủng hộ USDT TRC20" width="280">
</p>

## Giấy phép

MIT License

---

> [!CAUTION]
> **CHỈ DÙNG CHO MỤC ĐÍCH CÁ NHÂN — KHÔNG THƯƠNG MẠI.**
>
> - Repo này được tạo qua reverse-engineering nhằm mục đích nghiên cứu và liên thông cá nhân (interoperability) với thiết bị **bạn sở hữu**.
> - **KHÔNG** dùng cho mục đích thương mại dưới bất kỳ hình thức nào.
> - **Tự kiểm tra kỹ các quy định về sở hữu trí tuệ, điều khoản dịch vụ và pháp luật hiện hành** tại nơi bạn sinh sống **trước khi** sử dụng. Bạn tự chịu hoàn toàn trách nhiệm.
> - **KHÔNG** chia sẻ, phát tán, hay sử dụng để tấn công/chống phá/làm gián đoạn hệ thống Hunonic hoặc bất kỳ hệ thống nào.
> - Tác giả không chịu trách nhiệm cho bất kỳ thiệt hại hay hậu quả pháp lý nào phát sinh từ việc sử dụng repo này.
