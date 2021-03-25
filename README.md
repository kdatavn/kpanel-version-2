### Lệnh Cài Đặt KPANEL Trên Centos 6 & 7 & 8:
```
bash <( curl -k https://kdata.vn/install )
```
test
----------------------------------------------

### Phiên bản hệ điều hành khuyên dùng:
- [x] **`CentOS 7 x64` Khuyên dùng để cho hiệu suất tốt nhất. Mã nguồn KPANEL hiện tại đang phát triển chính trên CentOS 7 x64.**
- [ ] `CentOS 8 x64` MỚI và đang thử nghiệm. Tương lai gần KPANEL cũng sẽ phát triển song song cả trên CentOS 8 x64, hiện tại mới đang thử nghiệm.
- [ ] `CentOS 6 x64` KPANEL được phát triển trên phiên bản CentOS 6 x64, do KPANEL kế thừa mã nguồn của kpanel nên KPANEL cũng hoạt động tốt trên CentOS 6 x64, nên nếu có yêu cầu bắt buộc phải dùng CentOS 6 thì bạn có thể hoàn toàn yên tâm sử dụng, chỉ là về lâu dài thì các phiên bản cũ sẽ trờ nên lỗi thời, nên KPANEL chỉ phát triển từ CentOS 7 & 8.
----------------------------------------------

> 2021/03/25
- Hệ điều hành `CentOS 8 x64` chỉ hỗ trợ các phiên bản PHP (7.2, 7.3, 7.4 và mới nhất là 8.0), nên khi chọn phiên bản thấp hơn các phiên bản này trong tính năng chuyển phiên bản PHP, KPANEL sẽ mặc định cài lại PHP phiên bản 7.2.
- PHP phiên bản 8.0 đang được thử nghiệm và sẽ sớm được cập nhật cho KPANEL.

----------------------------------------------

### Danh sách các phiên bản kết hợp đã qua quá trình cài đặt thử nghiệm thành công:
> Với `CentOS 6 x64` đã chạy thực nghiệm từ nhiều năm nay và cho kết quả ổn định, nên ở mục này chủ yếu thống kê cho phiên bản CentOS 7 & 8 và KPANEL cũng chỉ hỗ trợ phiên bản x64 chứ không hỗ trợ x32 như KPANEL bản gốc.

> 2020/09/14
- [x] CentOS-**7** x64 && Nginx-1.18.0 + OpenSSL-1.1.1i + Prce-8.44 + Zlib-1.2.11 && PHP-7.4
- [x] **MariaDB-10.2** --- Cấu hình khuyên dùng ---------------------------------------------------

> 2020/09/15
- [x] CentOS-**7** x64 && Nginx-1.18.0 + OpenSSL-1.1.1i + Prce-8.44 + Zlib-1.2.11 && PHP-7.4
- [x] **MariaDB-10.4**

> 2020/09/15
- [x] CentOS-**7** x64 && Nginx-1.18.0 + OpenSSL-1.1.1i + Prce-8.44 + Zlib-1.2.11 && PHP-7.4
- [ ] **MariaDB-10.5**

> 2020/09/14
- [x] CentOS-**7** x64 && Nginx-1.18.0 + OpenSSL-1.1.1i + Prce-8.44 + Zlib-1.2.11 && PHP-7.4
- [x] **MariaDB-10.1**

> 2020/09/14
- [x] CentOS-**7** x64 && Nginx-1.18.0 + OpenSSL-1.1.1i + Prce-8.44 + Zlib-1.2.11 && PHP-7.4
- [x] **MariaDB-10.3**

----------------------------------------------

> 2020/09/19
- [x] CentOS-**8** x64 && Nginx-1.18.0 + OpenSSL-1.1.1i + Prce-8.44 + Zlib-1.2.11 && PHP-7.4
- [x] **MariaDB-10.3**

> 2020/09/19
- [x] CentOS-**8** x64 && Nginx-1.18.0 + OpenSSL-1.1.1i + Prce-8.44 + Zlib-1.2.11 && PHP-7.4
- [ ] **MariaDB-10.4**

> 2020/09/19
- [x] CentOS-**8** x64 && Nginx-1.18.0 + OpenSSL-1.1.1i + Prce-8.44 + Zlib-1.2.11 && PHP-7.4
- [ ] **MariaDB-10.5**

----------------------------------------------

### Loại bỏ phiên bản MariaDB 10.0 và MariaDB 5.5
> 2020/10/19
Lâu không dùng 2 bản cũ kia, mà nọ có việc nên xem lại câu lệnh từ phiên bản đó thấy nó cổ lỗ sĩ hơn cả MySQL nên mình quyết định loại bỏ thẳng tay luôn

### Varnish Cache
> 2020/09/11
#### Thêm chức năng cài đặt Varnish Cache: https://packagecloud.io/varnishcache/
#### Ngoài việc sử dụng KPANEL làm VPS chạy website thông thường, giờ đây bạn cũng có thể sử dụng để làm VPS chạy Varnish Cache rất tiện dụng. Hiện tại mình đang chạy thành công trên Varnish 4.1, bản 6.xx mới hơn chút xíu nhưng mình chưa thử nghiệm ngon lành, nên khuyên dùng vẫn là Varnish 4.1
#### Mã thực thi: https://github.com/kdatavn/kpanel-version-2/tree/main/script/kpanel/menu/varnish
> Cách sử dụng: Trong KPANEL menu -> 25) Tien ich - Addons -> 23) Varnish Cache -> Chọn phiên bản Varnish mà bạn muốn cài đặt
#### Không nên sử dụng VPS vừa làm VPS cache vừa làm VPS chạy web để tránh các xung đột không cần thiết.

----------------------------------------------

### OpenSSL
> 2020/09/01
#### Cập nhật OpenSSL lên bản mới nhất và build nginx từ bản này: https://linuxscriptshub.com/update-openssl-1-1-0-centos-6-9-7-0/
#### Mã thực thi: https://github.com/kdatavn/kpanel-version-2/blob/main/script/kpanel/menu/nang-cap-openssl
> Cách sử dụng: Trong KPANEL menu -> 26) Update System -> 7) Thay phien phien ban OpenSSL

----------------------------------------------

### Nginx
> 2020/09/01
#### Nguồn cài đặt: https://github.com/kdatavn/kpanel-version-2/blob/main/script/kpanel/nginx-setup.conf
- Cài đặt nginx-1.18.0, đây là phiên bản ổn định và mới nhất của nginx tính đến thời điểm hiện tại, kết hợp với OpenSSL-1.1.1i thay cho bản openssl cũ của KPANEL, phiên bản này mới hỗ trợ đầy đủ HTTP/2.
	- Phiên bản nginx được xem và cập nhật tại: http://nginx.org/en/download.html . Mặc định mình chỉ chọn phiên bản Stable version, các bản Mainline là đang phát triển nên không chọn.
	- Chuyển sang sử dụng OpenSSL-1.1.1i, đây cũng là bản openssl mới nhất hiện nay. Hỗ trợ HTTP/2 hoàn chỉnh, TLSv1.3 và rất nhiều cải tiến khác so với các bản tiền nhiệm. Các phiên bản OpenSSL khác có thể xem thêm tại đây: https://www.openssl.org/source/
	- https://ftp.pcre.org/pub/pcre/ -> dùng bản 8.44 thay cho bản 8.39 của KPANEL.
	- https://www.zlib.net/ -> dùng bản 1.2.11 thay cho bản 1.2.8 của KPANEL.

----------------------------------------------

> 2020/08/29
#### Loại bỏ phiên bản MariaDB 5 do có vẻ nó đã lỗi thời, với lại mấy năm nay mình dùng bản MariaDB 10 thấy rất ổn định nên cũng khuyên dùng.

----------------------------------------------

> 2020/08/27
- Cho bạn lựa chọn MariaDB phiên bản 10.3, 10.2, 10.1, 10.0 và bản 5.5 thay vì bản 10.0 và 5.5 mặc định của KPANEL. Tự động config phù hợp với cấu hình server.
- Lựa chọn 6 phiên bản PHP : 7.2, 7.1, 7.0, 5.6, 5.5 hoặc 5.4. KPANEL tự động config tối ưu PHP tùy theo cấu hình VPS và thay bạn có thể thay đổi PHP version thoải mái trong quá trình sử dụng.
- Loại bỏ memcached trong quá trình cài đặt mặc định, cái này ai thấy cần thiết thì cài thêm là được. Giờ Server/ VPS thường thuê là hàng chạy ổ SSD cũng rất nhanh, nên mình dùng Cache trên ổ cứng cho nó kinh tế hơn nhiều mà tốc độ tải không chậm hơn so với RAM là bao nhiêu.
- Loại bỏ CSF trong quá trình cài đặt mặc định, về cơ bản thì CSF khá tốn RAM, ai có VPS hoặc server RAM khỏe thì bấm cài thêm thủ công. Sau khi cài xong VPS các bạn nên đổi SSH port đi, điều này cũng tránh được khá nhiều phiền toái cho VPS mà lại nhẹ. Đổi SSH port bằng cách vào menu số 25) Tien ich - Addons -> 13) Thay Doi Port SSH Number.
- Còn lại hầu hết các tính năng vẫn được giữ nguyên hoặc chưa có thời gian chỉnh sửa, bổ sung...