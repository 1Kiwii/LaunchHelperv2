# 🎮 Minecraft Server Launcher Wrapper

A **lightweight Java launcher wrapper** for Minecraft servers — perfect for hosting panels like **Pterodactyl**!  
Customize JVM args, remap commands (like `stop` → `end` for BungeeCord), and get slick Discord webhook alerts on server start/stop.

---

## 📜 License

This project is licensed under the MIT License.  
Feel free to use, modify, and share — just give credit!

---

## 🚀 Features

- **Custom JVM arguments** via `launcher.properties`  
- **Command remapping** with `remap.properties` (optional & secret)  
- **Discord webhook support** (`launcher-webhook.properties`) with clean embed messages  
- Proxy console input/output, so your server runs smoothly  
- **Standalone `.jar`** — no external dependencies!

---

## 🛠 Getting Started

### 1. Upload Files

- Upload `Launcher.jar` to your server’s working directory.  
- Create or upload these config files:  

  - `launcher.properties`  
    ```properties
    java -javaagent:authlibinjector.jar=ely.by -jar server.jar
    ```

  - `launcher-webhook.properties` (optional)  
    ```properties
    webhookUrl=https://discord.com/api/webhooks/your_webhook_url_here
    ```

  - `remap.properties` (optional, you have to create the file on your own)  
    ```properties
    stop=end
    restart=stop
    ```

---

### 2. Configure Pterodactyl

Set your startup command to:  
```bash
java -jar Launcher.jar
```

Made with 💖 by [Rarfield](https://youtube.com/@Rarfield)
