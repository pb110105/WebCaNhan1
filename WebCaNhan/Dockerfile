# Sử dụng Nginx nhẹ, chuyên phục vụ web tĩnh
FROM nginx:alpine

# Xóa file mặc định của nginx
RUN rm -rf /usr/share/nginx/html/*

# Copy toàn bộ nội dung web (HTML, CSS, JS, hình ảnh, v.v.)
COPY . /usr/share/nginx/html

# Mở cổng 80 để truy cập
EXPOSE 80

# Lệnh khởi chạy mặc định của nginx
CMD ["nginx", "-g", "daemon off;"]