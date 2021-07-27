---
order: 1
title:
  zh-CN: Windows 下 Firefox 原生滚动条占位问题
  en-US: Firefox scrollbar need extract space
---

## zh-CN

Windows Firefox 及 IE 浏览器，滚动条并非脱离文档会占据空间，导致内容无法自适应显示

对应 Issue: https://github.com/ant-design/ant-design/issues/29528

## en-US

Windows Firefox 及 IE 浏览器，滚动条并非脱离文档会占据空间，导致内容无法自适应显示

对应 Issue: https://github.com/ant-design/ant-design/issues/29528

```jsx
import { Select } from 'antd';

const { Option } = Select;

function onChange(value) {
  console.log(`selected ${value}`);
}

function onBlur() {
  console.log('blur');
}

function onFocus() {
  console.log('focus');
}

function onSearch(val) {
  console.log('search:', val);
}

ReactDOM.render(
  <Select style={{ width: 200 }} placeholder="Select a person" dropdownMatchSelectWidth={false}>
    <Option value="davinci">Leonardo di ser Piero da Vinci</Option>
    <Option value="jack">Jack</Option>
    <Option value="lucy">Lucy</Option>
    <Option value="jerry">Jerry</Option>
    <Option value="kid">Kid</Option>
    <Option value="tomas">Tomas</Option>
    <Option value="lingard">Lingard</Option>
    <Option value="jim">Jim</Option>
    <Option value="paul">Paul</Option>
    <Option value="book">Book</Option>
  </Select>,
  mountNode,
);
```
