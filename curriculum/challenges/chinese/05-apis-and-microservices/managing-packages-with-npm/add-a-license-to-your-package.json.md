---
id: 587d7fb4367417b2b2512bfe
title: 给 package.json 添加许可证
challengeType: 2
forumTopicId: 301523
---

# --description--

license 字段是你告知用户允许他们拿这个项目干什么的地方。

常见的开源协议是 MIT 和 BSD。如果你想了解更多适合你项目的许可证的信息，那么 `http://choosealicense.com` 是一个不错的网站。

许可证信息并不是必须的。大多数国家的版权法会默认让你拥有自己创作的作品的所有权。但是，明确说明用户可以做什么和不能做什么会是一个很好的做法。

以下是一个 license 字段的示例：

\`\`\`json

"license": "MIT",

\`\`\`

# --instructions--

在 Glitch 项目的 package.json 中填写合适的 license 字段。

# --hints--

package.json 应该有一个有效的 'license' 键。

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/package.json').then(
    (data) => {
      var packJson = JSON.parse(data);
      assert(packJson.license, '"license" is missing');
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

# --solutions--

