# 昆仑F5摄影作品分享网站部署指南

## 项目概述
昆仑F5是一个邀请制的高质量摄影社区，支持照片和视频作品展示、分类浏览和社交互动功能。

## 域名配置
- 域名：kunlunF5.com
- DNS记录：已配置CNAME文件

## 部署方式

### 方法一：GitHub Pages 部署（推荐）
1. 将项目推送到GitHub仓库
2. 在仓库设置中启用GitHub Pages
3. 选择部署分支（通常为main或master）
4. 配置自定义域名：kunlunF5.com
5. 等待DNS配置生效（通常需要24-48小时）

### 方法二：Vercel 部署
1. 注册并登录Vercel账号
2. 导入项目仓库
3. 在项目设置中配置自定义域名
4. 按照Vercel提供的DNS配置指南更新域名服务器

### 方法三：Netlify 部署
1. 注册并登录Netlify账号
2. 拖拽项目文件夹或连接Git仓库
3. 在站点设置中添加自定义域名
4. 按照Netlify提供的DNS记录配置域名

## 服务器部署（可选）

### Nginx 配置示例
```nginx
server {
    listen 80;
    server_name kunlunF5.com www.kunlunF5.com;
    
    root /var/www/kunlunF5.com;
    index index.html;
    
    location / {
        try_files $uri $uri/ =404;
    }
    
    # 启用HTTPS（推荐）
    listen 443 ssl;
    ssl_certificate /path/to/ssl/certificate.crt;
    ssl_certificate_key /path/to/ssl/private.key;
}
```

### Apache 配置示例
```apache
<VirtualHost *:80>
    ServerName kunlunF5.com
    ServerAlias www.kunlunF5.com
    DocumentRoot /var/www/kunlunF5.com
    
    <Directory /var/www/kunlunF5.com>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
```

## HTTPS 配置
为了网站安全和SEO优化，强烈建议配置HTTPS：

1. 从Let's Encrypt获取免费SSL证书
2. 或购买商业SSL证书
3. 在服务器配置中启用SSL/TLS
4. 配置HTTP到HTTPS的重定向

## 性能优化建议
1. 启用Gzip/Brotli压缩
2. 配置浏览器缓存
3. 使用CDN加速静态资源
4. 图片懒加载和响应式图片
5. 启用HTTP/2

## 维护说明
- 定期备份网站文件和数据
- 监控网站访问日志和性能
- 及时更新依赖库和框架
- 定期检查域名和SSL证书状态

## 联系方式
如有部署问题，请联系技术支持。