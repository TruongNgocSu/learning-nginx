---------->>>> Nginx <<<<----------
1. Cấu trúc thư mục cơ bản được cài đặt tại "/etc/nginx", cần lưu ý một vài điểm.
 - Thư mục sites-availableà chứa các site định nghĩa virtual host server. Nhưng vẫn chưa thể truy cập được.
 - Thư mục sites-enabled sẽ public các site này vào config của nginx vì trong config chính của nginx có import thư mục này vào.
 - File "nginx.conf" là file cấu hình chính, file này có các context như:
      + Mail context
      + Upstream context
      + Http context
      + Events context
      + Main
 Note: File full config trên trang chủ "https://www.nginx.com/resources/wiki/start/topics/examples/full/".
2. cấu hình cơ bản nginx đối vs 1 web tĩnh:
 - Phải đặt trong context http ( file etc/sites-enabled/web1 duoc import ben trong context http).
 - Cấu hình cơ bản xem trong file etc/sites-enabled/web1
 - Và để truy cập được vào virtual host svrver thì phải add server_name của server và IP vào trong file etc/hosts/ file này là file mặc định của ubuntu

 Note:
 - https://www.digitalocean.com/community/tutorials/understanding-nginx-server-and-location-block-selection-algorithms
 - https://www.plesk.com/blog/various/nginx-configuration-guide/#:~:text=Every%20NGINX%20configuration%20file%20will,interchangeably%20as%20blocks%20or%20contexts%20.