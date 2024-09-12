# Hướng dẫn chi tiết cách cài đặt Ollama để sử dụng Large Language Model (LLM) mã nguồn mở ngay trên máy tính của bạn

## Giới thiệu

Bạn muốn trải nghiệm sức mạnh của các mô hình ngôn ngữ lớn (LLM) mã nguồn mở mà không cần kết nối internet hay phụ thuộc vào API của bên thứ ba? Ollama chính là giải pháp hoàn hảo dành cho bạn!
Ollama là một công cụ cho phép bạn tải xuống và chạy các LLM mã nguồn mở ngay trên máy tính của mình một cách dễ dàng. Hãy cùng Chip AI tìm hiểu cách cài đặt và sử dụng Ollama qua các bước sau nhé!

## Yêu cầu hệ thống

* **RAM:** 8GB cho mô hình 3B, 16GB cho mô hình 7B, 32GB cho mô hình 13B.
* **Dung lượng đĩa:** Dung lượng để lưu trữ dữ liệu mô hình, tùy thuộc vào mô hình bạn sử dụng.
* **CPU:** Khuyến nghị CPU có ít nhất 4 lõi. Với mô hình 13B, khuyến nghị CPU có ít nhất 8 lõi.
* **GPU (Tùy chọn):** GPU không bắt buộc để chạy Ollama, nhưng nó có thể cải thiện hiệu suất, đặc biệt là khi chạy các mô hình lớn hơn.

## Các bước cài đặt

1. **Tải xuống và cài đặt Ollama:** [https://ollama.com/download](https://ollama.com/download)
2. **Tải xuống mô hình LLM:** Bạn có thể thể xem các mô hình LLMs tại đây [https://ollama.com/library](https://ollama.com/library). ollama pull <tên mô hình>, ví dụ: ollama pull llama3.1
3. **Chạy mô hình LLM:** `ollama run <tên mô hình>. Ví dụ: ollama run llama3.1
4. **Tương tác với mô hình LLM:** Nhập văn bản và nhấn Enter.

## Sử dụng giao diện người dùng (UI)

1. **Tải xuống và cài đặt Docker Desktop:** [https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)
2. **Tải và cài đặt Open WebUI thông qua docker:** 
   ```bash
   docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main

Bây giờ bạn có thể thoải mái tận hưởng những con AI của riêng mình ở máy tính cá nhân mà hoàn toàn không cần lo ngại về các vấn đề liên quan đến privacy data tại http://localhost:3000

![image](https://github.com/user-attachments/assets/5dcf435c-eca0-456f-bb09-1f237c4e79ec)

## Nếu máy tính của bạn có GPU thì hãy chạy lệnh sau để tăng hiệu năng sử dụng

1. **Chạy câu lệnh sau:**
   ```bash
   docker run -d -p 3000:8080 --gpus=all -v ollama:/root/.ollama -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:ollama

## Kết luận
Ollama là một công cụ mạnh mẽ cho phép bạn trải nghiệm sức mạnh của các LLM mã nguồn mở ngay trên máy tính của mình. Hy vọng bài viết này sẽ giúp bạn cài đặt và sử dụng Ollama một cách dễ dàng.

## Happy ChipAI!! ##


