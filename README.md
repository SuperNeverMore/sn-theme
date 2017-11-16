# sn-theme
### variables.less
### 定义主题变量的less文件
--整体修改主题样式时需要改变的变量，定义整体风格

包含:
+ 公共前缀
```
@prefix: sn-;

```

+ 主要颜色： 
```
// 字体颜色
@font-color: #333;
@dark-p-color: #898989;
// 背景色
@base-background-color: #fefefe;
@dark-background-color: #1c1c1c;
@base-color: #55B761;

@--primary: @base-background-color;
@--success: #13ce66;
@--warning: #f7ba2a;
@--danger: #EE3133;//#ff4949;
@--info: #80BDFF;//#50bfff;
@--accessory: #b26cb2;
// 边框颜色
@base-border-color: @base-background-color;
@border-color: #495057;
@dark-border-color: #d8d8d8;
// link
@link-color: @base-color;
```

+ 基本尺寸： 
```

@tinny: --tinny;
@small: --small;
@large: --large;
```

+ 不同类型
```
@primary: --primary;
@success: --success;
@warning: --warning;
@danger: --danger;
@info: --info;
@accessory: --accessory;

```

*******
### common.less
### 定义公共样式
公共引用less文件

定义body  a button input box-shadow radius等基本样式

具体颜色、尺寸后缀引用variables.less文件
```
a{
    color: @font-color;
    &:hover{
        color:@base-color;
    }
}
button.@{prefix}btn {
    .radius;
    padding: 9px 15px;
    font-size:14px;
    &:not(.is-disabled):hover{
        transform: translateY(-2px);
        transition: transform 0.2s cubic-bezier(0.165, 0.84, 0.44, 1), color 0.2s ease-in-out;
    }
    .color-hover-primary(@border-color);
    &@{danger}{
        background-color: @@danger;
        .color-hover(@@danger)
    }
    &@{accessory}{
        background-color: @@accessory;
        .color-hover(@@accessory)
    }
    &@{warning}{
        background-color: @@warning;
        .color-hover(@@warning)
    }
    &@{primary}{
        .color-hover(@base-color);
    }
    &@{tinny}{
        padding: 2px 6px;
        font-size:12px;
    }
    &@{small}{
        padding: 4px 10px;
        font-size:12px;
    }
    &@{large}{
        padding: 10px 20px;
        font-size:16px;
    }
}
```
