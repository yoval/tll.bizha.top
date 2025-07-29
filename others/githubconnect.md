# github 连接

---

- 查看是否设置了代理：

        git config --global http.proxy
        git config --global https.proxy

- 关闭设置代理

        git config --global --unset http.proxy
        git config --global --unset https.proxy

- 设置代理

        git config --global http.proxy 'socks5://127.0.0.1:7890'
        git config --global https.proxy 'socks5://127.0.0.1:7890'


