---
title: Zotero链接Obsidian多设备一致性
date: 2025-04-26
last_modified_at: 2025-04-26
categories: [tool]
tags: [obsidian, zotero]
toc:  true
---

今天我踩了个大坑，关于obsidian链接zotero的问题。分享给经常多设备工作又有同样联动需求的朋友，避免踩坑。

在obsidian中的zotlit的connect里面设置zetero必须是全局路径。由于我的zotero和obsidian都放在了onedrive上所以如果不同电脑的user的名字不一样，那zetero的路径是不一样的。而user这个名字不随我登陆微软邮箱而改变的，系统激活的时候设置了就定了，后续改起来非常麻烦，需要修改注册表等，参考知乎[帖子](https://zhuanlan.zhihu.com/p/509804656)。所以我想实现两设备的一致，得改一台电脑的注册表，将user的名字改成一样的。

虽然抓狂，不过也只能接受，毕竟obsidian这种比较隐私的个人知识库，也不会在随便一台电脑部署，必须是自己常用的机器才会有这个需求。

---

Want to see something else added? <a href="https://github.com/MingshuoXu/MingshuoXu.github.io/issues/new">Open an issue.</a>

[^fn-sample_footnote]: Handy! Now click the return link to go back.
