# Buổi 1. Giới thiệu ngành lập trình và chương trình đầu tiên

Created: May 27, 2022 4:45 PM
Last Edited Time: May 31, 2022 9:17 AM
Status: In Progress
Type: Technical Spec

# Mục tiêu buổi học

Cài đặt thành công các công cụ để sẵn sàng lập trình ứng dụng di động.

Chạy được ứng dụng đầu tiên.

# Cài đặt công cụ

Đây là các công cụ được sử dụng trong suốt khóa học

## 1. Visual Studio Code

- Tải về tại [https://code.visualstudio.com](https://code.visualstudio.com/)
- Sau khi tải về file cài đặt, bạn tiến hành cài đặt chương trình trên máy tính.
- Đây là công cụ được sử dụng để viết mã chương trình, bạn sẽ làm việc thường xuyên trên công cụ này.

## 2. Android Studio

- Tải về tại [https://developer.android.com/studio](https://developer.android.com/studio)
- Sau khi tải về file cài đặt, bạn tiến hành cài đặt chương trình trên máy tính.
- Đây là công cụ bổ trợ cho việc chuyển đổi mã nguồn sang thiết bị điện thoại Android.

## 3. Node

- Tải về tại link: [https://nodejs.org/en](https://nodejs.org/en)
- Sau khi tải về file cài đặt, bạn tiến hành cài đặt chương trình trên máy tính.
- Đây là công cụ biên dịch mã nguồn Javascript

## 4. Yarn & NPX

- Chạy lệnh trong Terminal (xem [hướng dẫn mở ứng dụng Terminal](https://www.notion.so/H-ng-d-n-s-d-ng-Terminal-adb81a94f4af4ffbb8ceb12e633f7808))

```bash
npm install --global yarn
npm i -g npx
```

## 5. Cấu hình biến môi trường **ANDROID_HOME**

- Mở [Setting] > [Advance System Setting] > [Environment Variables]

![Screen Shot 2022-05-30 at 14.44.12.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_14.44.12.png)

![Screen Shot 2022-05-30 at 14.37.27.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_14.37.27.png)

![Screen Shot 2022-05-30 at 14.37.51.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_14.37.51.png)

- Tại [User variables for <username>] > chọn [New] > nhập tên biến là [ANDROID_HOME] và  giá trị là đường dẫn tương ứng trên máy tính của bạn > [OK]

![Screen Shot 2022-05-30 at 14.40.22.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_14.40.22.png)

## 6. Thêm **platform-tools vào path**

- Thực hiện tương tự ở mục 5, chọn [Path] > [Edit]

![Screen Shot 2022-05-30 at 14.46.15.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_14.46.15.png)

- Chọn [New] và  nhập đường dẫn

```bash
%LOCALAPPDATA%\Android\Sdk\platform-tools
```

![Screen Shot 2022-05-30 at 14.46.30.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_14.46.30.png)

- Chọn [OK] và lưu lại cài đặt.

## 7.  Tạo máy ảo Android

[Tham khảo tại đây](https://www.notion.so/H-ng-d-n-t-o-m-y-o-Android-f74411c40c914f79936b08382b5fc394)

# Tạo ứng dụng đầu tiên

Mở ứng dụng [Command Prompt]  > chạy lệnh bên dưới để tạo dự án ReactNative đầu tiên

```bash
npx react-native init HitekApp
```

<aside>
💡 [Hitek App] là tên dự án mà bạn tạo, bạn có thể chọn 1 tên bất kỳ. Lưu ý không chứa khoảng trắng trong tên

</aside>

<aside>
💡 Nếu xảy ra lỗi khi thực hiện lệnh trên, hãy kiểm tra lại phiên bản node của bạn cần lớn hơn v12, thực hiện lệnh “node -v” để kiểm tra

</aside>

Nếu dòng lệnh xuất hiện thông báo yêu cầu cài đặt [react-native], bạn nhấn [y] > [Enter]

![Screen Shot 2022-05-30 at 14.57.19.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_14.57.19.png)

- Tạo ứng dụng thành công

![Screen Shot 2022-05-30 at 15.19.54.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_15.19.54.png)

Chuyển hướng vào folder dự án bằng cách chạy lệnh sau

```bash
cd HitekApp
```

Chạy lệnh sau để tải các công cụ bổ trợ cho dự án

```bash
yarn
```

Chạy dịch vụ Metro bằng lệnh sau

```bash
npx react-native start
```

![Screen Shot 2022-05-30 at 15.44.15.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_15.44.15.png)

Mở công cụ [Terminal] trên một cửa sổ mới, di chuyển đến folder dự án và thực hiện lệnh bên dưới để khởi chạy ứng dụng

```bash
npx react-native run-android
```

Sau khi chạy lệnh, ứng dụng sẽ được mở tự động trên máy ảo

![Screen Shot 2022-05-30 at 15.48.13.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_15.48.13.png)

![Screen Shot 2022-05-30 at 15.49.52.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_15.49.52.png)

# Chạy ứng dụng bằng công cụ Visual Studio Code

- Mở ứng dụng VS Code
- Chọn [File] > [Open Folder] > Chọn folder dự án
    
    ![Screen Shot 2022-05-30 at 15.55.56.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_15.55.56.png)
    
- Mở [Terminal] trên VSCode: [Terminal] > [New Terminal]
- Chạy lệnh

```bash
npx react-native start
```

- Mở cửa sổ [Terminal] mới
    
    ![Screen Shot 2022-05-30 at 15.58.26.png](Buo%CC%82%CC%89i%201%20Gio%CC%9B%CC%81i%20thie%CC%A3%CC%82u%20nga%CC%80nh%20la%CC%A3%CC%82p%20tri%CC%80nh%20va%CC%80%20ch%20b3d205d063c24e11b091967fd0ebccfc/Screen_Shot_2022-05-30_at_15.58.26.png)
    

- Chạy lệnh

```bash
npx react-native run-android
```

- Sau khi thực hiện lệnh trên, ứng dụng được tự động mở trên máy ảo Android