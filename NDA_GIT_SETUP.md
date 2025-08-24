# NDA Git Setup Guide - NDA Git设置指南

## 🔒 NDA合规的Git配置

### 重要说明
本项目出于NDA（保密协议）要求，只能上传 `hvac-energy-optimizing-demo` 文件夹的内容到Git仓库。其他包含敏感信息的文件夹必须保持在本地，不能上传。

### 已配置的保护措施

#### 1. .gitignore 文件配置
已在 `.gitignore` 文件中添加了以下敏感文件夹的排除规则：
```
../invention-patent-application/
../midasII-archive-ai-knowledge-backup/
../midasII-mysql-db-backup/
../midasII-runtime-java/
../Model.Main.v0/
../Model.Training.v0/
../plc-and-intouch/
../venv-midasii-archive/
```

#### 2. 敏感文件类型排除
```
*.doc, *.docx, *.xlsx, *.xls, *.rar, *.zip, *.7z, *.sql, *.bak, *.backup
```

### Git操作指南

#### 初始化仓库（如果还没有）
```bash
cd hvac-energy-optimizing-demo
git init
git remote add origin https://github.com/grekyin/hvac-energy-optimizing-demo.git
```

#### 检查状态
```bash
git status
```
确保只显示 `hvac-energy-optimizing-demo` 文件夹内的文件

#### 添加文件
```bash
git add .
```
这只会添加当前文件夹内的文件

#### 提交更改
```bash
git commit -m "Update: [描述你的更改]"
```

#### 推送到远程仓库
```bash
git push origin main
```

### 验证NDA合规性

#### 检查将要上传的文件
```bash
git diff --cached --name-only
```
确保列表中不包含任何敏感文件夹或文件

#### 检查远程仓库内容
在推送前，可以检查远程仓库的当前内容：
```bash
git ls-remote origin
```

### 注意事项

1. **永远不要** 从根目录运行 `git add .`
2. **永远不要** 将敏感文件夹添加到Git
3. **定期检查** `git status` 确保没有意外添加敏感文件
4. **使用相对路径** 在代码中引用敏感数据时，确保路径正确

### 敏感信息处理

- **专利文档**: 保持在 `../invention-patent-application/` 本地
- **AI知识备份**: 保持在 `../midasII-archive-ai-knowledge-backup/` 本地
- **数据库备份**: 保持在 `../midasII-mysql-db-backup/` 本地
- **Java运行时**: 保持在 `../midasII-runtime-java/` 本地
- **模型文件**: 保持在 `../Model.Main.v0/` 和 `../Model.Training.v0/` 本地
- **PLC配置**: 保持在 `../plc-and-intouch/` 本地

### 紧急情况处理

如果意外添加了敏感文件：
```bash
# 从暂存区移除
git reset HEAD [敏感文件路径]

# 从工作区移除（如果文件还没有提交）
git checkout -- [敏感文件路径]

# 如果已经提交，需要回滚
git reset --hard HEAD~1
```

---

**记住：NDA合规是最高优先级，宁可不上传也不要冒险上传敏感信息！**
