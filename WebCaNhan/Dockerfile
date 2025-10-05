# Sử dụng image Nginx nhẹ
FROM nginx:alpine

# Xóa trang mặc định của Nginx
RUN rm -rf /usr/share/nginx/html/*

# Copy toàn bộ mã nguồn web vào thư mục HTML của Nginx
COPY . /usr/share/nginx/html

# Mở cổng 10000 (Render yêu cầu PORT phải được set qua biến môi trường)
EXPOSE 10000

# Cấu hình Nginx để dùng biến môi trường PORT (Render bắt buộc)
CMD ["sh", "-c", "sed -i 's/listen       80;/listen       ${PORT:-10000};/' /etc/nginx/conf.d/default.conf && nginx -g 'daemon off;'"]
