create-tauri-app@4.5.2

## flow

pnpm create tauri-app

ncu -i

pnpm i

pnpm tauri android init (需要 android 环境)

端口冲突，修改下端口。

Windows 系统需要开启 开发者模式。

调整 `src-tauri\tauri.conf.json` build.beforeDevCommand 使安卓模拟器可以访问开发服务器。
否则可能出现 `error sending request for url(http://localhost:11420/)`。
`--host` 可以使 Vite 将监听所有可用的网络接口（0.0.0.0）。

pnpm tauri android dev

### Android 打包流程

使用 keytool 生成 Keystore 文件 xxx.jks

修改 `[project]/src-tauri/gen/android/[your-app]/key.properties`

## log

```
$ pnpm create tauri-app
✔ Project name · template-tauri-v2-mobile-create-way
✔ Identifier · com.template-tauri-v2-mobile-create-way.app
✔ Choose which language to use for your frontend · TypeScript / JavaScript - (pnpm, yarn, npm, deno, bun)
✔ Choose your package manager · pnpm
✔ Choose your UI template · React - (https://react.dev/)
✔ Choose your UI flavor · TypeScript

Template created! To get started run:
  cd template-tauri-v2-mobile-create-way
  pnpm install
  pnpm tauri android init

For Desktop development, run:
  pnpm tauri dev

For Android development, run:
  pnpm tauri android dev


```
