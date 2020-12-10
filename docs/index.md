## I. Liferay 7.x blank portlet release

**Yêu cầu hệ thống:**

- Liferay 7.x server. Tải [server Liferay 7.1](https://sourceforge.net/projects/lportal/files/Liferay%20Portal/7.1.0%20GA1/)

- Postgres 9.6 (Khuyên dùng)
- Node js (phiên bản mới nhất)



Tải server Liferay 7.x về giải nén sau đó vào thư mục `/webapps` chạy lệnh:

```bash
git clone https://github.com/ttdathub/liferay-blank-portlet.git SamplePortlet
```

![Git clone command](.\assets\images\portlet-clone-cmd.PNG)

**Portlet được cài đặt sẵn:**

- JSF 2.2.15
- Primefaces 8
- Gson
- Lombok
- Log4j
- Guava-r05
- Apache POI 3.15
- Hibernate 5.5.2
- Flyway
- Webpack & Laravel mix

**Sử dụng webpack**

Run command to install dependencies.

```bash
npm install
```

**Java Build Path**

Import portlet vào eclipse và import JDK cùng các thư viện trong thư mục `/dev/lib` và `/WEB-INF/lib` => Build and start Liferay

![Portlet structure](.\assets\images\blank-portlet-structure.PNG)

**Tạo file cấu hình build nhanh**

Vào thư mục `~/tomcat-9.0.10/conf/Catalina/localhost` tạo file `SamplePortlet.xml` với nội dung như sau:

```xml
<Context reloadable="true" />
```



Portlet sẽ tự động deploy khi ta build lại thay vì deploy bằng file *.war

Start server:

![](.\assets\images\server-started.PNG)
