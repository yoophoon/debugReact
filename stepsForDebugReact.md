# debug react源码的步骤
> 主要参考[React 之如何调试源码](https://juejin.cn/post/7168821587251036167?from=search-suggest)
## 准备react项目
### 初始化项目
```powershell
npx create-react-app react-app
cd react-app
```
### 弹出配置文件
```powershell
npm run eject
```
### 克隆react源码
因为react-create-app不允许访问src文件夹外的资源，所以源码需要克隆到src目录下
```powershell
cd src
git clone git@github.com:facebook/react.git

# 采用submodule的方式不用将react仓库上传到本仓库
git submodule add git@github.com:facebook/react.git react
# 克隆时采用git clone git@github.com:yoophoon/debugReact.git --recurse-submodules
# 即可将仓库及其子模块一起克隆至本地git clone && git submodule update
```
## 配置项目
### 调整react版本
```powershell
# 项目采用的是react@v18.3.1
git checkout v18.3.1
```

