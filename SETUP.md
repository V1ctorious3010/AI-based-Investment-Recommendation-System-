# Cài đặt và Chạy Hệ thống Quản lý Tài sản

## Yêu cầu hệ thống

- Docker & Docker Compose
- Node.js 18+ (để chạy script khởi tạo dữ liệu)
- Python 3.9+ (để chạy AI service riêng lẻ nếu cần)

## Cách 1: Chạy toàn bộ hệ thống bằng Docker (Khuyến nghị)

### Bước 1: Clone và cài đặt

### Bước 2: Kiểm tra các service

### Bước 3: Khởi tạo dữ liệu mẫu


### Bước 4: Truy cập ứng dụng
- **Frontend**: http://localhost:3000
- **API Gateway**: http://localhost:8000
- **Customer Service**: http://localhost:8001
- **Asset Service**: http://localhost:8002
- **Market Data Service**: http://localhost:8003
- **AI Service**: http://localhost:8004

## Cách 2: Chạy từng service riêng lẻ

### Bước 1: Cài đặt dependencies


### Bước 2: Khởi động cơ sở dữ liệu


### Bước 3: Chạy các service



## API Endpoints

### Customer Service (Port 8001)
- `GET /api/customers` - Lấy danh sách khách hàng
- `GET /api/customers/:id` - Lấy thông tin khách hàng
- `POST /api/customers` - Tạo khách hàng mới
- `PUT /api/customers/:id` - Cập nhật khách hàng
- `DELETE /api/customers/:id` - Xóa khách hàng

### Asset Service (Port 8002)
- `GET /api/assets` - Lấy danh sách tài sản
- `GET /api/assets/customer/:customerId` - Lấy tài sản theo khách hàng
- `POST /api/assets` - Tạo tài sản mới
- `PUT /api/assets/:id` - Cập nhật tài sản
- `DELETE /api/assets/:id` - Xóa tài sản

### AI Service (Port 8004)
- `POST /api/ai/recommendations` - Lấy gợi ý đầu tư
- `GET /api/ai/analysis/:customerId` - Phân tích danh mục
- `GET /api/ai/risk-assessment/:customerId` - Đánh giá rủi ro

### API Gateway (Port 8000)
- Tất cả API trên thông qua gateway
- `GET /api/dashboard/:customerId` - Dữ liệu dashboard tổng hợp

## Tính năng chính

### Frontend
- **Dashboard**: Tổng quan tài sản, biểu đồ phân bổ
- **Assets**: Quản lý tài sản, xem chi tiết
- **Recommendations**: Gợi ý đầu tư từ AI
- **Profile**: Thông tin khách hàng
- **Chatbot**: Hỗ trợ tương tác

### Backend
- **Microservice Architecture**: 5 service độc lập
- **AI Integration**: Machine learning cho gợi ý đầu tư
- **Real-time Updates**: Kafka message broker
- **Caching**: Redis cache
- **Database**: MongoDB

## Development

### Cấu trúc thư mục
```
1stWeb/
├── frontend/                 # React frontend
├── customer-service/         # Customer management
├── asset-service/           # Asset management
├── market-data-service/     # Market data
├── ai-recommendation-service/ # AI recommendations
├── api-gateway/             # API Gateway
├── scripts/                 # Utility scripts
├── docker-compose.yml       # Docker configuration
└── README.md               # Documentation
```



