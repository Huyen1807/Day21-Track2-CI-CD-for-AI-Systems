# Reflection

- Mục tiêu: Hoàn thiện pipeline CI/CD để huấn luyện, kiểm thử và triển khai mô hình.
- Những việc đã hoàn thành: implement `src/serve.py` (FastAPI), viết unit tests (`tests/test_train.py`), cấu hình workflow CI (`.github/workflows/mlops.yml`), fix MLflow URI cho Windows, upload model lên GCS và cấu hình systemd trên VM để chạy service.
- Kết quả: Unit tests chạy thành công; pipeline chạy qua các bước test/train/eval; service `mlops-serve` trên VM đã được bật và trả về health OK.
- Khó khăn chính: accuracy của mô hình hiện ~0.67, thấp hơn ngưỡng 0.70; nguyên nhân khả dĩ là thiếu dữ liệu hoặc cần thử mô hình/hyperparameter khác.
- Bước tiếp theo khuyến nghị: (1) thêm dữ liệu bằng `add_new_data.py` và rerun DVC push, (2) thử thuật toán khác (GradientBoosting/ExtraTrees) hoặc tinh chỉnh hyperparameters, (3) thêm giám sát và logging cho mô hình production.

Người thực hiện: Nguyễn Thị Thanh Huyền
Ngày: 2026-05-07
