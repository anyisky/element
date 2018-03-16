<style>
  .demo-bg-box{
    display: flex;
    flex-wrap: wrap;
    div{
      width: 240px;
      border-radius: 4px;
      padding: 20px;
      box-sizing: border-box;
      color: #fff;
      font-size: 14px;
      margin-bottom:10px;
      margin-right:10px;
    }
  }
  .boder-demo{
    div{
      padding: 20px;
    }
  }

  .boxshadow-demo{
    div{
      padding: 20px;
    }
  }
</style>

## Color 色彩

为了方便开发使用相关颜色值的变量，分别列举出来。

### 基础变量 scss
```css
/* Colors
-------------------------- */
$--color-white: #fff !default;
$--color-black: #000 !default;

$--color-primary: #00BCD6 !default; 
$--color-primary-light-1: mix($--color-white, $--color-primary, 10%) !default; /* 1ac3da */
$--color-primary-light-2: mix($--color-white, $--color-primary, 20%) !default; /* 33c9de */
$--color-primary-light-3: mix($--color-white, $--color-primary, 30%) !default; /* 4dd0e2 */
$--color-primary-light-4: mix($--color-white, $--color-primary, 40%) !default; /* 66d7e6 */
$--color-primary-light-5: mix($--color-white, $--color-primary, 50%) !default; /* 80deeb */
$--color-primary-light-6: mix($--color-white, $--color-primary, 60%) !default; /* 99e4ef */
$--color-primary-light-7: mix($--color-white, $--color-primary, 70%) !default; /* b3ebf3 */
$--color-primary-light-8: mix($--color-white, $--color-primary, 80%) !default; /* ccf2f7 */
$--color-primary-light-9: mix($--color-white, $--color-primary, 90%) !default; /* e6f8fb */

$--color-success: #4cb050 !default;
$--color-warning: #F7BA2A !default;
$--color-danger: #ff4159 !default;
$--color-info: #909399 !default;

$--color-success-light: mix($--color-white, $--color-success, 80%) !default;
$--color-warning-light: mix($--color-white, $--color-warning, 80%) !default;
$--color-danger-light: mix($--color-white, $--color-danger, 80%) !default;
$--color-info-light: mix($--color-white, $--color-info, 80%) !default;

$--color-success-lighter: mix($--color-white, $--color-success, 90%) !default;
$--color-warning-lighter: mix($--color-white, $--color-warning, 90%) !default;
$--color-danger-lighter: mix($--color-white, $--color-danger, 90%) !default;
$--color-info-lighter: mix($--color-white, $--color-info, 90%) !default;

$--color-text-primary: #263238 !default;
$--color-text-regular: #455a64 !default;
$--color-text-secondary: #b0bec5 !default;
$--color-text-placeholder: #cfd8dc !default;

/* Link
-------------------------- */
$--link-color: $--color-primary-light-2 !default;
$--link-hover-color: $--color-primary !default;

/* Background
-------------------------- */
$--background-color-base: #f5f7fa !default;

/* Border
-------------------------- */
$--border-width-base: 1px !default;
$--border-style-base: solid !default;
$--border-color-base: #dcdfe6 !default;
$--border-color-light: #e4e7ed !default;
$--border-color-lighter: #ebeef5 !default;
$--border-color-extra-light: #f2f6fc !default;
$--border-color-hover: $--color-text-placeholder !default;
$--border-base: $--border-width-base $--border-style-base $--border-color-base !default;
$--border-radius-base: 2px !default;
$--border-radius-small: 2px !default;
$--border-radius-circle: 100% !default;

/* Box-shadow
-------------------------- */
$--box-shadow-base: 0 2px 4px rgba(0, 0, 0, .12), 0 0 6px rgba(0, 0, 0, .04) !default;
$--box-shadow-dark: 0 2px 4px rgba(0, 0, 0, .12), 0 0 6px rgba(0, 0, 0, .12) !default;
$--box-shadow-light: 0 2px 12px 0 rgba(0, 0, 0, 0.1) !default;
```

### 字体色

:::demo
```html
<div style="margin: 20px 0">
  <div class="bg-primary txt-white">白色 #ffffff</div>
  <div class="txt-black">黑色 #000000</div>
  <br>
  <div class="txt-primary">主色 #00BCD6</div>
  <div class="txt-primary-light1">主色 混白色 10% #1ac3da</div>
  <div class="txt-primary-light2">主色 混白色 20% #33c9de</div>
  <div class="txt-primary-light3">主色 混白色 30% #4dd0e2</div>
  <div class="txt-primary-light4">主色 混白色 40% #66d7e6</div>
  <div class="txt-primary-light5">主色 混白色 50% #80deeb</div>
  <div class="txt-primary-light6">主色 混白色 60% #99e4ef</div>
  <div class="txt-primary-light7">主色 混白色 70% #b3ebf3</div>
  <div class="txt-primary-light8">主色 混白色 80% #ccf2f7</div>
  <div class="txt-primary-light9">主色 混白色 90% #e6f8fb</div>
  <br>
  <div class="txt-success">success #4cb050</div>
  <div class="txt-warning">warning #F7BA2A</div>
  <div class="txt-danger">danger #ff4159</div>
  <div class="txt-info">info #909399</div>
  <br>
  <div class="txt-success-light">success 混白色 80% #dbefdc</div>
  <div class="txt-warning-light">warning 混白色 80% #fdf1d4</div>
  <div class="txt-danger-light">danger 混白色 80% #ffd9de</div>
  <div class="txt-info-light">info 混白色 80% #e9e9eb</div>
  <br>
  <div class="txt-success-lighter">success 混白色 90% #edf7ee</div>
  <div class="txt-warning-lighter">warning 混白色 90% #fef8ea</div>
  <div class="txt-danger-lighter">danger 混白色 90% #ffecee</div>
  <div class="txt-info-lighter">info 混白色 90% #f4f4f5</div>
  <br>
  <div class="txt-grey-primary">灰色 #263238</div>
  <div class="txt-grey-regular">灰色regular #455a64</div>
  <div class="txt-grey-secondary">灰色secondary #b0bec5</div>
  <div class="txt-grey-placeholder">灰色placeholder #cfd8dc</div>
  <br>
  <div><a href="javascript:;" class="txt-link">链接 #33c9de</a></div>
  <div><a href="javascript:;" class="txt-link-hover">链接hover时 #00BCD6</a></div>
</div>
```
:::

### 背景色

:::demo
```html
<div style="margin: 20px 0" class="demo-bg-box">
  <div class="bg-base" style="color:#00BCD6">基础背景色 #f5f7fa</div>
  <div class="bg-white" style="border:1px solid #00BCD6;color:#00BCD6">白色 #ffffff</div>
  <div class="bg-black">黑色 #000000</div>
  <div class="bg-primary">主色 #00BCD6</div>
  <div class="bg-primary-light1">主色 混白色 10% #1ac3da</div>
  <div class="bg-primary-light2">主色 混白色 20% #33c9de</div>
  <div class="bg-primary-light3">主色 混白色 30% #4dd0e2</div>
  <div class="bg-primary-light4">主色 混白色 40% #66d7e6</div>
  <div class="bg-primary-light5">主色 混白色 50% #80deeb</div>
  <div class="bg-primary-light6">主色 混白色 60% #99e4ef</div>
  <div class="bg-primary-light7">主色 混白色 70% #b3ebf3</div>
  <div class="bg-primary-light8">主色 混白色 80% #ccf2f7</div>
  <div class="bg-primary-light9">主色 混白色 90% #e6f8fb</div>
  <div class="bg-success">success #4cb050</div>
  <div class="bg-warning">warning #F7BA2A</div>
  <div class="bg-danger">danger #ff4159</div>
  <div class="bg-info">info #909399</div>
  <div class="bg-success-light">success 混白色 80% #dbefdc</div>
  <div class="bg-warning-light">warning 混白色 80% #fdf1d4</div>
  <div class="bg-danger-light">danger 混白色 80% #ffd9de</div>
  <div class="bg-info-light">info 混白色 80% #e9e9eb</div>
  <div class="bg-success-lighter">success 混白色 90% #edf7ee</div>
  <div class="bg-warning-lighter">warning 混白色 90% #fef8ea</div>
  <div class="bg-danger-lighter">danger 混白色 90% #ffecee</div>
  <div class="bg-info-lighter">info 混白色 90% #f4f4f5</div>
  <div class="bg-grey-primary">灰色 #263238</div>
  <div class="bg-grey-regular">灰色regular #455a64</div>
  <div class="bg-grey-secondary">灰色secondary #b0bec5</div>
  <div class="bg-grey-placeholder">灰色placeholder #cfd8dc</div>
</div>
```
:::

### 字号

:::demo
```html
<div style="margin: 20px 0">
  <div class="ky-font-base">基础字号 14px</div>
  <div class="ky-font-small">small字号 13px</div>
  <div class="ky-font-large">large字号 18px</div>
</div>
```
:::

### 边框色

:::demo
```html
<div style="margin: 20px 0" class="boder-demo">
  <div class="bd-base">基础色边框 #dcdfe6</div>
  <br>
  <div class="bd-light">light 边框 #e4e7ed</div>
  <br>
  <div class="bd-lighter">lighter 边框 #ebeef5</div>
  <br>
  <div class="bd-extra-light">extra-light 边框 #f2f6fc</div>
</div>
```
:::

### 边框阴影

:::demo
```html
<div style="margin: 20px 0" class="boxshadow-demo">
  <div class="bd-base box-shadow-base">基础色边框阴影</div>
  <br>
  <div class="bd-base box-shadow-dark">dark 边框阴影</div>
  <br>
  <div class="bd-base box-shadow-light">light 边框阴影</div>
</div>
```
:::
