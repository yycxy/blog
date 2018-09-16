---
title: "deepClone"
date: 2018-09-16T19:26:52+08:00
tags: ["js"]
categories: ["js"]
---

## 深拷贝


```
function deepCopy(data) {
   const t = this.typeOf(data);
   let o;

   if (t === 'array') {
       o = [];
   } else if (t === 'object') {
       o = {};
   } else {
       return data;
   }

   if (t === 'array') {
       for (let i = 0; i < data.length; i++) {
           o.push(this.deepCopy(data[i]));
       }
   } else if (t === 'object') {
       for (let i in data) {
           o[i] = this.deepCopy(data[i]);
       }
   }
   return o;
};
```