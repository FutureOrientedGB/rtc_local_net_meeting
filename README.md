# 1. install tauri util
```
cargo install tauri-cli
cargo install create-tauri-app --locked
```

# 2. prepare tauri apps

## 2.1. create app

### 2.1.1. create app from template
```
cargo create-tauri-app --manager cargo --template vanilla app
```

### 2.1.2. change app's identifier
```
 app\src-tauri\tauri.conf.json
   - bundle - identifier
   > com.future-oriented-gb.local-net-meeting
```
   
### 2.1.3. change app's product name
```
 app\src-tauri\tauri.conf.json
   - package - productName
   > local-net-meeting
```
   
### 2.1.4. change app's window title
```
 app\src-tauri\tauri.conf.json
	- tauri - windows - title
	> local net meeting
```
	
### 2.1.5. build exe and installer
```
cd app
cargo tauri build
```

### 2.1.6. find outputs
```
exe > app/src-tauri/target/release/local-net-meeting.exe
msi > app/src-tauri/target/release/bundle/msi/local-net-meeting_0.0.0_x64_en-US.msi
nsis > app/src-tauri/target/release/bundle/nsis/local-net-meeting_0.0.0_x64-setup.msi
```
	
