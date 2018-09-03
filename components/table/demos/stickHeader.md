---
title: 表头吸顶
order: 8.1 
---

`stickHeader`：设置表头是否当表格滚动超出规定高度时，将表头固定在页面顶部，类型`Boolean` | `Number`，默认：`false`

1. 如果取值为`Boolean`，`false`表示不吸顶，`true`表示吸顶，此时等价于`0`，标示固定的位置的`top`为`0`
2. 如果取值为`Number`，用来指定固定的高度`top`，例如本例中，固定在`top = 50px`的地方

> 指定了该属性，则`fixHeader`属性没有意义了

```vdt
import {Table, TableColumn} from 'kpc/components/table';

const data = [
    {name: 'Javey', sex: 'male'},
    {name: 'Lisa', sex: 'female'}
];

<Table data={{ data }} stickHeader="50">
    <TableColumn title="姓名" key="name">
        <b:template params="data">
            {{ data.name }}
        </b:template>
    </TableColumn>
    <TableColumn title="性别" key="sex">
        <b:template params="data">
            {{ data.sex }}
        </b:template>
    </TableColumn>
</Table>
```