---
title: <Router>.history
sidebar_label: history
---

```tsx
const { history } = createRouter({
  home: defineRoute("/"),
  post: defineRoute({ postId: "path.param.string" }, p => `/post/${p.postId}`)
});

history.goBack();
history.goForward();
```

The `history` property of a router provides direct access to the underlying history instance from the [core library](https://github.com/ReactTraining/history) which powers Type Route. Most use cases won't require using this property. If you do need to access it, do so with caution as certain uses may cause unexpected behavior.