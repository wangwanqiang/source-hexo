---
title: Git的两步提交
id: 170
categories:
  - 未分类
tags:
---

1).从工作目录，提交到stage。
2).从stage提交到master。

从工作目录提交到stage，需要用add或者rm命令，只提交到stage，而没有提交到master，是不会自动同步到master的。

从stage提交到master用commit命令。

退回也是要分两步，一个是从master退回到stage，然后再从stage退回到工作目录。

对于还没有提交到stage的，可以从stage用checkout命令退回，这一步会取stage中的文件状态，覆盖掉工作目录中文件的状态，跟master完全没关系。

对于已经到达stage的，想把state中的文件状态用master中的覆盖掉，就用reset命令，这样就把stage中修改用master的状态覆盖掉了，完全跟工作目录没关系