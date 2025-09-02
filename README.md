# Wuji Hand Upgrader

Wuji HMI 应用程序 - 用于机器人灵巧手升级的桌面应用

## 系统要求

- **操作系统**: Linux (Ubuntu 18.04, Ubuntu 20.04, Ubuntu 22.04)
- **架构**: x86_64 (AMD64)
- **依赖**: libtbb2

## 安装方式

### 方式一：Snap（推荐）

Snap 是由 Canonical 推出的 Linux 下的通用软件包格式，常见Linux系统的软件商店即可安装。

#### 安装步骤

1. 打开Linux软件商店（Ubuntu Software）

2. 搜索 wujihand-upgrader

3. 点击安装,等待安装完成

4. 安装完成后需要点击Permissions按钮然后打开系统权限

   - Access hardware infomation

   - Access USB hardware directly

5. 运行应用程序（首次打开加载应用程序可能时间较长，请耐心等待）


### 方式二：AppImage

AppImage 是一种便携式应用程序格式，无需安装即可运行。

#### 下载
从以下地址下载最新版本的 AppImage 文件：
- GitHub Releases：https://github.com/Wuji-Technology-Co-Ltd/wujihand-upgrader-hmi/releases

#### 安装步骤

1. **下载 AppImage 文件**
   ```bash
   wget https://github.com/Wuji-Technology-Co-Ltd/wujihand-upgrader-hmi/releases/download/v1.3.2/wujihand-upgrader-1.3.2.AppImage
   ```

2. **添加执行权限**
   ```bash
   chmod +x wujihand-upgrader-1.3.2.AppImage
   ```

3. **运行应用程序**
   ```bash
   ./wujihand-upgrader-1.3.2.AppImage
   ```

### 方式三：Debian 包 (.deb)

Debian 包提供系统级安装，适合需要集成到系统菜单的用户。

#### 下载
下载对应版本的 .deb 文件：
- GitHub Releases：https://github.com/Wuji-Technology-Co-Ltd/wujihand-upgrader-hmi/releases

#### 安装步骤

1. **下载 .deb 文件**
   ```bash
   wget https://github.com/Wuji-Technology-Co-Ltd/wujihand-upgrader-hmi/releases/download/v1.3.2/wujihand-upgrader_1.3.2_amd64.deb
   ```

2. **安装依赖**
   ```bash
   sudo apt update
   sudo apt install libtbb2
   ```

3. **安装应用程序**
   ```bash
   sudo apt install wujihand-upgrader_1.3.2_amd64.deb
   ```

4. **运行应用程序**
   ```bash
   wujihand-upgrader
   ```

#### 卸载
```bash
sudo apt remove wujihand-upgrader
```

## 故障排除

### 常见问题

1. **AppImage 无法运行**
   ```bash
   # 检查文件权限
   ls -la wujihand-upgrader-*.AppImage
   
   # 重新添加执行权限
   chmod +x wujihand-upgrader-*.AppImage
   ```

2. **依赖缺失错误**
   ```bash
   # 安装必要的依赖
   sudo apt update
   sudo apt install libtbb2 libtbb-dev -y
   ```
---

**注意**: 首次运行可能需要较长时间来解压和初始化应用程序。请耐心等待。

