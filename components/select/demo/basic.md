---
order: 0
title:
  zh-CN: 虚拟滚动与 dropdownMatchSelectWidth 共存
  en-US: virtual scroll with dropdownMatchSelectWidth
---

## zh-CN

当 `dropdownMatchSelectWidth = false` 时使用虚拟滚动似乎并没有问题

相关 issue：https://github.com/ant-design/ant-design/issues/21754

## en-US

```jsx
import { Select } from 'antd';

const { Option } = Select;

function handleChange(value) {
  console.log(`selected ${value}`);
}

ReactDOM.render(
  <>
    <div>
      <Select
        defaultValue="lucy"
        dropdownMatchSelectWidth={false}
        style={{ width: 120 }}
        onChange={handleChange}
      >
        ·<Option value="jack">Jack</Option>
        <Option value="lucy">Lucddddddddddddddddddy</Option>
        <Option value="disabled" disabled>
          Disabled
        </Option>
        <Option value="Yiminghe">yiminghe</Option>
      </Select>
    </div>
    <div>
      <Select
        defaultValue="lucy"
        dropdownMatchSelectWidth={false}
        // style={{ width: 120 }}
        onChange={handleChange}
      >
        <Option value="jack">Jack</Option>
        <Option value="lucy">Lucddddddddddddddddddy</Option>
        <Option value="disabled" disabled>
          Disabled
        </Option>
        <Option value="Yiminghe">yiminghe</Option>
      </Select>
    </div>
  </>,
  mountNode,
);
```
