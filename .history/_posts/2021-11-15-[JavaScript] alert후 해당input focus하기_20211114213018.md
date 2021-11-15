---
layout: single
title: "[JavaScript] alert후 해당input focus하기"
---

```html
<input type="text" class="w_130" id="inp_name" v-model="userNm">
```

```jsx
// alert이후에 input focus
function validation(){
    if(name == null || name == ""){
        alert("이름을 입력해주세요");
        document.getElementById('inp_name').focus();
    }
}
```