# Wuji Hand Upgrader

Wuji HMI 应用程序 - 用于机器人灵巧手升级的桌面应用

## 系统要求

- **操作系统**: Linux (Ubuntu 18.04+)
- **架构**: x86_64 (AMD64)

## 安装方式

### Debian 包 (.deb)（推荐）

Debian 包提供系统级安装，适合需要集成到系统菜单的用户。安装后会自动配置串口权限和用户组。

#### 下载
下载对应版本的 .deb 文件：
- GitHub Releases：https://github.com/Wuji-Technology-Co-Ltd/wujihand-upgrader-hmi/releases

#### 安装步骤

1. **下载 .deb 文件**
   ```bash
   wget https://github.com/Wuji-Technology-Co-Ltd/wujihand-upgrader-hmi/releases/download/v2.0.0/wujihand-upgrader_2.0.0_amd64.deb
   ```

2. **使用 dpkg 安装应用程序**
   ```bash
   sudo dpkg -i wujihand-upgrader_2.0.0_amd64.deb
   # 如遇依赖问题可执行
   sudo apt-get install -f
   ```

3. **运行应用程序**
   
   在桌面端点击“WUJI”APP图标运行

#### 权限配置
安装完成后，系统会自动：
- 开放串口设备访问权限
- 将当前用户添加到相应的用户组
- 配置必要的硬件访问权限

#### 时序要求
固件升级时，需要满足以下时序：
1. 灵巧手处于断电状态，先打开wuji hmi应用程序
2. 灵巧手先通过USB连接到PC，然后再给灵巧手通电
3. wuji hmi会自动连接到灵巧手引导程序
4. 正常连接后可进行固件升级操作

**注意**：若连接后提示当前不处于引导程序，需要重新给灵巧手上电

#### 卸载
```bash
sudo dpkg -r wujihand-upgrader
```

## 故障排除

### 常见问题

1. **依赖缺失错误**
   ```bash
   # 安装必要的依赖
   sudo apt update
   sudo apt install libtbb2 libtbb-dev libtbb12 -y
   ```
---

**注意**: 首次运行可能需要较长时间来解压和初始化应用程序。请耐心等待。



