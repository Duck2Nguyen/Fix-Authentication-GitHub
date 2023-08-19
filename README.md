# Fix-Authentication-GitHub
Fix Authentication GitHub


~ Loại bõ token cũ
Về cơ bản thông tin đăng nhập của bạn đã hết hạn và bạn cần xóa nó đi:
Chạy lại 2 lệnh command sau: 
  git config --global --unset credential.helper
  git config credential.helper store
  
~Tạo token github
  Đăng nhập vào github của bạn rồi vào link sau: https://github.com/settings/tokens.
  Bấm vô gennerate new token
  Đặt đại cái tên rồi chọn vào 3 mục lớn: repo, workflow, gist
  ![image](https://github.com/Duck2Nguyen/Fix-Authentication-GitHub/assets/72493095/edc208f3-5954-42c1-87e6-873054ae34ab)

~Cập nhật github repo

Nếu bạn clone thì sửa lại cái git thành dạng này:   
  git clone https://<token>@github.com/<username>/<tên repo>

Hoặc nếu bạn đã có repo thì dùng lệnh này để sửa lại cái repo
  git remote set-url origin https://<token>@github.com/<username>/< tên repo>
