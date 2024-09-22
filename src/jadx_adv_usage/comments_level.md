# 设置注释等级

jadx反编译代码中，出现提示：

```java
/*
    Method dump skipped, instructions count: 330
    To view this dump add '--comments-level debug' option
*/
```

可以用：

```bash
jadx --comments-level debug -d outputFolder yourAndroidApp.apk
```

去消除，且（应该是）可以输出更多注释信息 -> 便于分析代码逻辑。
