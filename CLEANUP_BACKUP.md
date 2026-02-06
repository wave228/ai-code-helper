# 高考志愿填报系统 - 清理备份清单

## 删除时间：2026-02-04
## 执行人：AI 助手

## 一、前端 API 删除清单

### university.js (保留5个，删除4个)
**保留：**
- getPageByFilterWithScores ✓
- getAll ✓
- searchByName ✓
- getUniversityFullDetail ✓
- getAdmissionScores ✓

**删除：**
- getById(id) - 根据ID查询院校
- getByCode(code) - 根据院校代码查询
- add(university) - 添加院校
- update(university) - 更新院校
- delete(id) - 删除院校

### major.js (保留1个，删除6个)
**保留：**
- getByUniversityCode ✓

**删除：**
- getAll() - 查询所有专业
- getPage(pageNum, pageSize) - 分页查询专业
- getById(id) - 根据ID查询专业
- searchByName(name) - 根据专业名称模糊查询
- add(majorInfo) - 添加专业
- update(majorInfo) - 更新专业
- delete(id) - 删除专业

### majorIntroduction.js (保留2个，删除7个)
**保留：**
- getMajorCategories ✓
- getMajorsByCategory ✓

**删除：**
- getPage(pageNum, pageSize) - 分页查询专业介绍
- searchByName(name) - 模糊查询专业介绍
- getById(id) - 根据ID查询专业介绍详情
- add(majorIntroduction) - 添加专业介绍
- update(majorIntroduction) - 更新专业介绍
- delete(id) - 删除专业介绍
- getUniversitiesByMajor(majorCode) - 根据专业代码查询院校

## 二、后端删除清单

### Controller 层 (删除3个)
1. MajorIntroductionController.java
2. UniversityDataController.java
3. UniversityTagUpdateController.java

### Service 层 (删除5个)
1. MajorIntroductionService.java
2. MajorIntroductionImportService.java
3. UniversityDataService.java
4. UniversityTagUpdateService.java
5. AiCodeHelper.java

### Mapper 层 (删除3个)
1. MajorIntroductionMapper.java
2. MajorCareerMapper.java
3. MajorCourseMapper.java

### AI 工具类 (删除2个)
1. InterviewQuestionTool.java
2. AdmissionRecommendationTool.java

### Entity 实体类 (删除4个)
1. MajorIntroduction.java
2. MajorIntroductionDetail.java
3. MajorCareer.java
4. MajorCourse.java

## 三、文件备份

所有删除的文件已备份到以下位置：
- 前端备份：e:\gitee\ai-demo\vue-gaokao-helper\backup_api_20260204
- 后端备份：e:\gitee\ai-demo\ai-code-helper\backup_backend_20260204

## 四、影响评估

**不影响的功能：**
- 院校查询和筛选 ✓
- 院校详情查看 ✓
- 录取分数查询 ✓
- AI 聊天助手 ✓
- 专业分类查询 ✓

**删除的功能：**
- 专业介绍管理（前端未使用）
- 院校数据导入（后端管理接口）
- 院校标签更新（后端管理接口）
- 旧版 AI 对话实现

## 五、注意事项

1. 如需恢复被删除的功能，请从备份目录还原
2. 后续如需专业介绍功能，需要重新实现前端界面
3. 保留了核心的高考志愿填报功能
4. 保留了完整的 AI 聊天助手功能
