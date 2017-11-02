# sn-theme
/*----------------------------------common.less----------------------------------*/
font-size:14px

button: small large
button: .btn-warn .btn-accessory

input :  small large

变量名称实例：
```bash
/*----------------------------------前缀----------------------------------*/
@prefix: sn-;
@primary: --primary;
@success: --success;
@warning: --warning;
@danger: --danger;
@info: --info;
@accessory: --accessory;
/*----------------------------------Colors------------------------------- */
// 字体颜色
@font-color: #333;
@dark-p-color: #898989;
// 背景色
@base-background-color: #fefefe;
@dark-background-color: #1c1c1c;
/*************基本颜色***************/
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
// link
@link-color: @base-color;
// 默认border-radius
@border-radius: 4px;
// 默认手势
@cursor: pointer;
/*-------------------------------button-------------------------------------*/
.color-hover(@color: @base-background-color) {
    background-color: @color;
    border: 1px solid @color;
    &:hover {
        background-color: darken(@color,8%);
        border: 1px solid darken(@color,8%);
    }
}
/*-------------------------------input-------------------------------------*/
@input-border: 2px solid rgba(0,0,0,0.15);
```