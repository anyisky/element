<script>
  export default {
    data() {
      return {
        list: null,
        options123: [],
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }, {
          value: '选项6',
          label: '黄金糕1'
        }, {
          value: '选项7',
          label: '双皮奶1'
        }, {
          value: '选项8',
          label: '蚵仔煎1'
        }, {
          value: '选项9',
          label: '龙须面1'
        }, {
          value: '选项10',
          label: '北京烤鸭1'
        }, {
          value: '选项11',
          label: '黄金糕2'
        }, {
          value: '选项12',
          label: '双皮奶2'
        }, {
          value: '选项13',
          label: '蚵仔煎2'
        }, {
          value: '选项14',
          label: '龙须面2'
        }, {
          value: '选项15',
          label: '北京烤鸭2'
        }, {
          value: '选项16',
          label: '黄金糕3'
        }, {
          value: '选项17',
          label: '双皮奶3'
        }, {
          value: '选项18',
          label: '蚵仔煎3'
        }, {
          value: '选项19',
          label: '龙须面3'
        }, {
          value: '选项20',
          label: '北京烤鸭3'
        }, {
          value: '选项21',
          label: '黄金糕4'
        }, {
          value: '选项22',
          label: '双皮奶4'
        }, {
          value: '选项23',
          label: '蚵仔煎4'
        }, {
          value: '选项24',
          label: '龙须面4'
        }, {
          value: '选项25',
          label: '北京烤鸭4'
        }, {
          value: '选项26',
          label: '黄金糕5'
        }, {
          value: '选项27',
          label: '双皮奶5'
        }, {
          value: '选项28',
          label: '蚵仔煎5'
        }, {
          value: '选项29',
          label: '龙须面5'
        }, {
          value: '选项30',
          label: '北京烤鸭5'
        }],
        options2: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶',
          disabled: true
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        options3: [{
          label: '热门城市',
          options: [{
            value: 'Shanghai',
            label: '上海'
          }, {
            value: 'Beijing',
            label: '北京'
          }]
        }, {
          label: '城市名',
          options: [{
            value: 'Chengdu',
            label: '成都'
          }, {
            value: 'Shenzhen',
            label: '深圳'
          }, {
            value: 'Guangzhou',
            label: '广州'
          }, {
            value: 'Dalian',
            label: '大连'
          }]
        }],
        options4: [],
        options5: [{
          value: 'HTML',
          label: 'HTML'
        }, {
          value: 'CSS',
          label: 'CSS'
        }, {
          value: 'JavaScript',
          label: 'JavaScript'
        }],
        cities: [{
          value: 'Beijing',
          label: '北京'
        }, {
          value: 'Shanghai',
          label: '上海'
        }, {
          value: 'Nanjing',
          label: '南京'
        }, {
          value: 'Chengdu',
          label: '成都'
        }, {
          value: 'Shenzhen',
          label: '深圳'
        }, {
          value: 'Guangzhou',
          label: '广州'
        }],
        value: '',
        hasValue: '选项3',
        value2: '',
        value3: '',
        value4: '',
        value5: [],
        value6: '',
        value7: '',
        value8: '',
        value9: '',
        value10: [],
        value11: [],
        loading: false,
        states: ["Alabama", "Alaska", "Arizona", "Arkansas", "California", "Colorado", "Connecticut", "Delaware", "Florida", "Georgia", "Hawaii", "Idaho", "Illinois", "Indiana", "Iowa", "Kansas", "Kentucky", "Louisiana", "Maine", "Maryland", "Massachusetts", "Michigan", "Minnesota", "Mississippi", "Missouri", "Montana", "Nebraska", "Nevada", "New Hampshire", "New Jersey", "New Mexico", "New York", "North Carolina", "North Dakota", "Ohio", "Oklahoma", "Oregon", "Pennsylvania", "Rhode Island", "South Carolina", "South Dakota", "Tennessee", "Texas", "Utah", "Vermont", "Virginia", "Washington", "West Virginia", "Wisconsin", "Wyoming"],
        selectValue: '',
        selectValueMult: [],
        hasSelectValue: 'aaa34',
        hasSelectValueMult: [1, 11, 33],
        originOptions: [], // 单选原始list
        originOptionsMult: [],// 多选原始list
        originOptionsHasValue: [], // 单选有值原始list
        originOptionsHasValueMult: [], // 多选有值原始list
        optionsListByFilter: [],
        optionsListByFilterMult: [],
        optionsListByFilterHasValue: [],
        optionsListByFilterHasValueMult: [],
        optionShowList: [],
        optionShowListMult: [],
        optionShowListHasValue: [],
        optionShowListHasValueMult: [],
        currentPage: 1,
        currentPageMult: 1,
        currentPageHasValue: 1,
        currentPageHasValueMult: 1,
        showPagination: true,
        showPaginationMult: true,
        showPaginationHasValue: true,
        showPaginationHasValueMult: true
      };
    },
    
    mounted() {
      this.list = this.states.map(item => { return { value: item, label: item }; });
    },

    created () {
      setTimeout(() => {
        this.value5 = ['选项1', '选项2', '选项3', '选项4', '选项5', '选项6', '选项7', '选项8', '选项9', '选项10', '选项11', '选项12', '选项13', '选项14', '选项15', '选项16', '选项17', '选项18', '选项19', '选项10', '选项21', '选项22', '选项23', '选项24', '选项25', '选项26', '选项27', '选项28', '选项29', '选项30']
      }, 0)
      for (let i = 0; i <= 1000; i++) {
        this.options123.push({value: 'aaa' + i + 1})
      }
      // 模拟数据，模拟 1000 条数据，用于示例远程搜索+分页
      for (let i = 0; i < 40; i++) {
        // this.originOptions.push({value: Number(i + 1), label: 'aaa' + Number(i + 1)})
        // 初始化四个原始数据
        this.originOptions.push({value: Number(i + 1), label: 'aaa' + Number(i + 1)})
        this.originOptionsMult.push({value: Number(i + 1), label: 'aaa' + Number(i + 1)})
        this.originOptionsHasValue.push({value: 'aaa' + Number(i + 1), label: 'aaa' + Number(i + 1)})
        this.originOptionsHasValueMult.push({value: Number(i + 1), label: 'aaa' + Number(i + 1)})
      }
      this.resetOptionsList()
      this.resetOptionsList('Mult')
      this.resetOptionsList('HasValue')
      this.resetOptionsList('HasValueMult')
    },

    methods: {
      remoteMethod(query) {
        if (query !== '') {
          this.loading = true;
          setTimeout(() => {
            this.loading = false;
            this.options4 = this.list.filter(item => item.label.toLowerCase().indexOf(query.toLowerCase()) > -1);
          }, 200);
        } else {
          this.options4 = [];
        }
      },
      checkAll () {
        this.value5 = ['选项1', '选项2', '选项3', '选项4', '选项5', '选项6', '选项7', '选项8', '选项9', '选项10', '选项11', '选项12', '选项13', '选项14', '选项15', '选项16', '选项17', '选项18', '选项19', '选项10', '选项21', '选项22', '选项23', '选项24', '选项25', '选项26', '选项27', '选项28', '选项29', '选项30']
      },
      resetOptionsList (type) { // 初始化数据
        if (type) {
          this['optionShowList' + type] = this['originOptions' + type].slice(0, 10)
        } else {
          this.optionShowList = this.originOptions.slice(0, 10)
        }
      },
      remoteMethodPageByType (query, type) {
        this['currentPage' + type] = 1
        if (query !== '') {
          this['optionsListByFilter' + type] = this['originOptions' + type].filter((item) => {
            return item.label.indexOf(query) > -1
          })
        } else {
          this['optionsListByFilter' + type] = this['originOptions' + type]
        }
        this['optionShowList' + type] = this['optionsListByFilter' + type].slice(0, this['currentPage' + type] * 10)
        this['showPagination' + type] = this['optionShowList' + type].length < this['optionsListByFilter' + type].length
      },
      remoteMethodPage (query) {
        this.remoteMethodPageByType(query, '')
      },
      remoteMethodPageMult (query) {
        this.remoteMethodPageByType(query, 'Mult')
      },
      remoteMethodPageHasValue (query) {
        this.remoteMethodPageByType(query, 'HasValue')
      },
      remoteMethodPageHasValueMult (query) {
        this.remoteMethodPageByType(query, 'HasValueMult')
      },
      loadMoreListByType (query, type) {
        if (!this['showPagination' + type]) {
          return false;
        }
        this['currentPage' + type]++;
        if (query !== '') {
          this['optionsListByFilter' + type] = this['originOptions' + type].filter((item) => {
            return item.label.indexOf(query) > -1
          })
        } else {
          this['optionsListByFilter' + type] = this['originOptions' + type]
        }
        this['optionShowList' + type] = this['optionsListByFilter' + type].slice(0, this['currentPage' + type] * 10)
        this['showPagination' + type] = this['optionShowList' + type].length < this['optionsListByFilter' + type].length
      },
      loadMoreList (query) {
        this.loadMoreListByType(query, '')
      },
      loadMoreListMult (query) {
        this.loadMoreListByType(query, 'Mult')
      },
      loadMoreListHasValue (query) {
        this.loadMoreListByType(query, 'HasValue')
      },
      loadMoreListHasValueMult (query) {
        this.loadMoreListByType(query, 'HasValueMult')
      },
      visibleChange (val) {
        this.currentPage = 1
        if (val) {
          this.resetOptionsList()
        }
      },
      visibleChangeMult (val) {
        this.currentPageMult = 1
        if (val) {
          this.resetOptionsList('Mult')
        }
      },
      visibleChangeHasValue (val) {
        this.currentPageHasValue = 1
        if (val) {
          this.resetOptionsList('HasValue')
        }
      },
      visibleChangeHasValueMult (val) {
        this.currentPageHasValueMult = 1
        if (val) {
          this.resetOptionsList('HasValueMult')
        }
      }
    }
  };
</script>

<style>
  .demo-select .el-select {
    width: 240px;
  }
  .demo-select .flexBox {
    padding: 0;
    display: flex;
  }
  .demo-select .block {
    padding: 30px 0;
    text-align: center;
    border-right: solid 1px #EFF2F6;
    flex: 1;
    &:last-child {
      border-right: none;
    }
  }

   .demo-select .demonstration {
    display: block;
    color: #8492a6;
    font-size: 14px;
    margin-bottom: 20px;
  }
</style>

## Select 选择器

当选项过多时，使用下拉菜单展示并选择内容。

:::tip
select和radio、checkbox一样，选中值和下拉选项中的值是===比较，必须类型和值都相同，才能匹配上，示例中就不做特殊展示了。
:::

### 基础用法

适用广泛的基础单选
:::demo `v-model`的值为当前被选中的`el-option`的 value 属性值
```html
<template>
  <el-select v-model="value" placeholder="请选择">
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
</template>

<script>
  export default {
    data() {
      return {
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value: ''
      }
    }
  }
</script>
```
:::

### 有选中值的用法

:::demo
```html
<template>
  <el-select v-model="hasValue" placeholder="请选择">
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
</template>

<script>
  export default {
    data() {
      return {
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        hasValue: '选项3'
      }
    }
  }
</script>
```
:::

### 有禁用选项

:::demo 在`el-option`中，设定`disabled`值为 true，即可禁用该选项
```html
<template>
  <el-select v-model="value2" placeholder="请选择">
    <el-option
      v-for="item in options2"
      :key="item.value"
      :label="item.label"
      :value="item.value"
      :disabled="item.disabled">
    </el-option>
  </el-select>
</template>

<script>
  export default {
    data() {
      return {
        options2: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶',
          disabled: true
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value2: ''
      }
    }
  }
</script>
```
:::

### 禁用状态

选择器不可用状态

:::demo 为`el-select`设置`disabled`属性，则整个选择器不可用
```html
<template>
  <el-select v-model="value3" disabled placeholder="请选择">
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
</template>
  
<script>
  export default {
    data() {
      return {
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value3: ''
      }
    }
  }
</script>
```
:::

### 可清空单选

包含清空按钮，可将选择器清空为初始状态

:::demo 为`el-select`设置`clearable`属性，则可将选择器清空。需要注意的是，`clearable`属性仅适用于单选。
```html
<template>
  <el-select v-model="value4" clearable placeholder="请选择">
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
</template>

<script>
  export default {
    data() {
      return {
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value4: ''
      }
    }
  }
</script>
```
:::

### 基础多选

适用性较广的基础多选，用 Tag 展示已选项

:::demo 为`el-select`设置`multiple`属性即可启用多选，此时`v-model`的值为当前选中值所组成的数组。默认情况下选中值会以 Tag 的形式展现，你也可以设置`collapse-tags`属性将它们合并为一段文字。
```html
<template>
  <el-button type="primary" @click="value5 = []">清空</el-button> <el-button type="primary" @click="checkAll">全选</el-button><br/>
  <br/>
  <el-select v-model="value5" multiple placeholder="请选择">
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>

  <el-select
    v-model="value11"
    multiple
    collapse-tags
    style="margin-left: 20px;"
    placeholder="请选择">
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
</template>

<script>
  export default {
    data() {
      return {
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value5: [],
        value11: []
      }
    }
  }
</script>
```
:::

### 自定义模板

可以自定义备选项

:::demo 将自定义的 HTML 模板插入`el-option`的 slot 中即可。
```html
<template>
  <el-select v-model="value6" placeholder="请选择">
    <el-option
      v-for="item in cities"
      :key="item.value"
      :label="item.label"
      :value="item.value">
      <i class="el-icon-edit" style="float: left"></i>
      <span style="float: left">{{ item.label }}</span>
      <span style="float: right; color: #8492a6; font-size: 13px">{{ item.value }}</span>
    </el-option>
  </el-select>
</template>

<script>
  export default {
    data() {
      return {
        cities: [{
          value: 'Beijing',
          label: '北京'
        }, {
          value: 'Shanghai',
          label: '上海'
        }, {
          value: 'Nanjing',
          label: '南京'
        }, {
          value: 'Chengdu',
          label: '成都'
        }, {
          value: 'Shenzhen',
          label: '深圳'
        }, {
          value: 'Guangzhou',
          label: '广州'
        }],
        value6: ''
      }
    }
  }
</script>
```
:::

### 分组

备选项进行分组展示

:::demo 使用`el-option-group`对备选项进行分组，它的`label`属性为分组名
```html
<template>
  <el-select v-model="value7" placeholder="请选择">
    <el-option-group
      v-for="group in options3"
      :key="group.label"
      :label="group.label">
      <el-option
        v-for="item in group.options"
        :key="item.value"
        :label="item.label"
        :value="item.value">
      </el-option>
    </el-option-group>
  </el-select>
</template>

<script>
  export default {
    data() {
      return {
        options3: [{
          label: '热门城市',
          options: [{
            value: 'Shanghai',
            label: '上海'
          }, {
            value: 'Beijing',
            label: '北京'
          }]
        }, {
          label: '城市名',
          options: [{
            value: 'Chengdu',
            label: '成都'
          }, {
            value: 'Shenzhen',
            label: '深圳'
          }, {
            value: 'Guangzhou',
            label: '广州'
          }, {
            value: 'Dalian',
            label: '大连'
          }]
        }],
        value7: ''
      }
    }
  }
</script>
```
:::

### 可搜索

可以利用搜索功能快速查找选项

:::demo 为`el-select`添加`filterable`属性即可启用搜索功能。默认情况下，Select 会找出所有`label`属性包含输入值的选项。如果希望使用其他的搜索逻辑，可以通过传入一个`filter-method`来实现。`filter-method`为一个`Function`，它会在输入值发生变化时调用，参数为当前输入值，可以通过 `slot` 设置 icon
```html
<template>
  <el-select v-model="value8" filterable placeholder="请选择">
    <i slot="prefix" class="el-input__icon el-icon-search"></i>
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
</template>

<script>
  export default {
    data() {
      return {
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value8: ''
      }
    }
  }
</script>
```
:::

### 远程搜索

从服务器搜索数据，输入关键字进行查找
:::demo 为了启用远程搜索，需要将`filterable`和`remote`设置为`true`，同时传入一个`remote-method`。`remote-method`为一个`Function`，它会在输入值发生变化时调用，参数为当前输入值。需要注意的是，如果`el-option`是通过`v-for`指令渲染出来的，此时需要为`el-option`添加`key`属性，且其值需具有唯一性，比如此例中的`item.value`。
```html
<template>
  <el-select
    v-model="value9"
    multiple
    filterable
    remote
    reserve-keyword
    placeholder="请输入关键词"
    :remote-method="remoteMethod"
    :loading="loading">
    <el-option
      v-for="item in options4"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
</template>

<script>
  export default {
    data() {
      return {
        options4: [],
        value9: [],
        list: [],
        loading: false,
        states: ["Alabama", "Alaska", "Arizona",
        "Arkansas", "California", "Colorado",
        "Connecticut", "Delaware", "Florida",
        "Georgia", "Hawaii", "Idaho", "Illinois",
        "Indiana", "Iowa", "Kansas", "Kentucky",
        "Louisiana", "Maine", "Maryland",
        "Massachusetts", "Michigan", "Minnesota",
        "Mississippi", "Missouri", "Montana",
        "Nebraska", "Nevada", "New Hampshire",
        "New Jersey", "New Mexico", "New York",
        "North Carolina", "North Dakota", "Ohio",
        "Oklahoma", "Oregon", "Pennsylvania",
        "Rhode Island", "South Carolina",
        "South Dakota", "Tennessee", "Texas",
        "Utah", "Vermont", "Virginia",
        "Washington", "West Virginia", "Wisconsin",
        "Wyoming"]
      }
    },
    mounted() {
      this.list = this.states.map(item => {
        return { value: item, label: item };
      });
    },
    methods: {
      remoteMethod(query) {
        if (query !== '') {
          this.loading = true;
          setTimeout(() => {
            this.loading = false;
            this.options4 = this.list.filter(item => {
              return item.label.toLowerCase()
                .indexOf(query.toLowerCase()) > -1;
            });
          }, 200);
        } else {
          this.options4 = [];
        }
      }
    }
  }
</script>
```
:::

### 结合远程搜索实现分页功能

注意：有个已知问题，当value 和label 不同时，带着默认选中值初始化时，显示的内容会是id，若value 和 label 一致，界面正常

:::demo 为了启用分页功能，需要将 `filterable` 和 `remote` 设置为 `true`，需要传入一个`remote-method`，`load-more-text`，`load-more-list`，`pagination`。`remote-method`为一个`Function`，它会在输入值发生变化时调用，参数为当前输入值。`load-more-text` 是字符串，用于显示加载更多选项的文案内容。`load-more-list`为一个`Function`，会在点击加载更多按钮时调用，参数是当前的输入值，根据当前输入值，以及页码值，进行重新赋值options列表。`pagination`用来控制是否显示加载更多按钮，当当前渲染的条数达到总记录数，就不显示加载更多按钮。
```html
<template>
<div class="demo-select">
  <div class="flexBox">
    <div class="block">
      <span class="demonstration">单选 Model 值： {{selectValue}}</span>
      <el-select v-model="selectValue" 
              placeholder="请选择" 
              filterable
              remote
              clearable
              @clear="resetOptionsList('')"
              @visible-change="visibleChange"
              :remote-method="remoteMethodPage"
              :pagination="showPagination" 
              :load-more-text="'加载更多'" 
              :load-more-list="loadMoreList">
        <el-option
          v-for="(item, $index) in optionShowList"
          :key="item.value"
          :label="item.label"
          :value="item.value">
        </el-option>
      </el-select>
    </div>
    <div class="block">
      <span class="demonstration">多选 Model 值： {{selectValueMult}}</span>
      <el-select v-model="selectValueMult" 
              placeholder="请选择" 
              filterable
              remote
              multiple
              @visible-change="visibleChangeMult"
              @remove-tag="resetOptionsList('Mult')"
              :remote-method="remoteMethodPageMult"
              :pagination="showPaginationMult" 
              :load-more-text="'加载更多'" 
              :load-more-list="loadMoreListMult">
        <el-option
          v-for="(item, $index) in optionShowListMult"
          :key="item.value"
          :label="item.label"
          :value="item.value">
        </el-option>
      </el-select>
    </div>
  </div>

  <div class="flexBox">
    <div class="block">
      <span class="demonstration">单选 有默认值 Model 值(value 和 label 值相同)： {{hasSelectValue}}</span>
      <el-select v-model="hasSelectValue" 
              placeholder="请选择" 
              filterable
              remote
              clearable
              @visible-change="visibleChangeHasValue"
              @clear="resetOptionsList('HasValue')"
              :remote-method="remoteMethodPageHasValue"
              :pagination="showPaginationHasValue" 
              :load-more-text="'加载更多'" 
              :load-more-list="loadMoreListHasValue">
        <el-option
          v-for="(item, $index) in optionShowListHasValue"
          :key="item.value"
          :label="item.label"
          :value="item.value">
        </el-option>
      </el-select>
    </div>

    <div class="block">
      <span class="demonstration">多选 有默认值 Model 值： {{hasSelectValueMult}}</span>
      <el-select v-model="hasSelectValueMult" 
              placeholder="请选择" 
              filterable
              remote
              multiple
              @visible-change="visibleChangeHasValueMult"
              @remove-tag="resetOptionsList('HasValueMult')"
              :remote-method="remoteMethodPageHasValueMult"
              :pagination="showPaginationHasValueMult" 
              :load-more-text="'加载更多'" 
              :load-more-list="loadMoreListHasValueMult">
        <el-option
          v-for="(item, $index) in optionShowListHasValueMult"
          :key="item.value"
          :label="item.label"
          :value="item.value">
        </el-option>
      </el-select>
    </div>
  </div>
</div>
  
</template>

<script>
  export default {
    data() {
      return {
        // 单选
        selectValue: '',
        originOptions: [], // 单选原始list
        optionsListByFilter: [], // 根据输入值过滤后的list
        optionShowList: [], // 实际显示在下拉中的list
        currentPage: 1, // 当前分页页码
        showPagination: true, // 是否显示加载按钮
        // 单选有默认值
        hasSelectValue: 'aaa34',
        originOptionsHasValue: [],
        optionsListByFilterHasValue: [],
        optionShowListHasValue: [],
        currentPageHasValue: 1,
        showPaginationHasValue: true,
        // 多选
        selectValueMult: '',
        originOptionsMult: [],
        optionsListByFilterMult: [],
        optionShowListMult: [],
        currentPageMult: 1,
        showPaginationMult: true,
        // 多选 没有默认值
        hasSelectValueMult: [1, 22, 44],
        originOptionsHasValueMult: [],
        optionsListByFilterHasValueMult: [],
        optionShowListHasValueMult: [],
        currentPageHasValueMult: 1,
        showPaginationHasValueMult: true
      }
    },
    mounted () {
      // 模拟数据，模拟 1000 条数据
      for (let i = 0; i < 40; i++) {
        // 初始化四个原始数据
        this.originOptions.push({value: Number(i + 1), label: 'aaa' + Number(i + 1)})
        this.originOptionsMult.push({value: Number(i + 1), label: 'aaa' + Number(i + 1)})
        this.originOptionsHasValue.push({value: 'aaa' + Number(i + 1), label: 'aaa' + Number(i + 1)})
        this.originOptionsHasValueMult.push({value: Number(i + 1), label: 'aaa' + Number(i + 1)})
      }
      this.resetOptionsList() // 初始化单选select
      this.resetOptionsList('Mult') // 初始化多选select
      this.resetOptionsList('HasValue') // 初始化有默认值的单选select
      this.resetOptionsList('HasValueMult') // 初始化有默认值的多选select
    },
    methods: {
      remoteMethodPageByType (query, type) {
        this['currentPage' + type] = 1
        if (query !== '') {
          this['optionsListByFilter' + type] = this['originOptions' + type].filter((item) => {
            return item.label.indexOf(query) > -1
          })
        } else {
          this['optionsListByFilter' + type] = this['originOptions' + type]
        }
        this['optionShowList' + type] = this['optionsListByFilter' + type].slice(0, this['currentPage' + type] * 10)
        this['showPagination' + type] = this['optionShowList' + type].length < this['optionsListByFilter' + type].length
      },
      loadMoreListByType (query, type) {
        if (!this['showPagination' + type]) {
          return false;
        }
        this['currentPage' + type]++;
        if (query !== '') {
          this['optionsListByFilter' + type] = this['originOptions' + type].filter((item) => {
            return item.label.indexOf(query) > -1
          })
        } else {
          this['optionsListByFilter' + type] = this['originOptions' + type]
        }
        this['optionShowList' + type] = this['optionsListByFilter' + type].slice(0, this['currentPage' + type] * 10)
        this['showPagination' + type] = this['optionShowList' + type].length < this['optionsListByFilter' + type].length
      },
      resetOptionsList (type) { // 初始化数据
        if (type) {
          this['optionShowList' + type] = this['originOptions' + type].slice(0, 10)
        } else {
          this.optionShowList = this.originOptions.slice(0, 10)
        }
      },
      // 单选
      remoteMethodPage (query) {
        this.remoteMethodPageByType(query, '')
      },
      loadMoreList (query) {
        this.loadMoreListByType(query, '')
      },
      visibleChange (val) {
        this.currentPage = 1
        if (val) {
          this.resetOptionsList()
        }
      },
      // 多选
      remoteMethodPageMult (query) {
        this.remoteMethodPageByType(query, 'Mult')
      },
      loadMoreListMult (query) {
        this.loadMoreListByType(query, 'Mult')
      },
      visibleChangeMult (val) {
        this.currentPageMult = 1
        if (val) {
          this.resetOptionsList('Mult')
        }
      },
      // 单选有默认值
      remoteMethodPageHasValue (query) {
        this.remoteMethodPageByType(query, 'HasValue')
      },
      loadMoreListHasValue (query) {
        this.loadMoreListByType(query, 'HasValue')
      },
      visibleChangeHasValue (val) {
        this.currentPageHasValue = 1
        if (val) {
          this.resetOptionsList('HasValue')
        }
      },
      // 多选有默认值
      remoteMethodPageHasValueMult (query) {
        this.remoteMethodPageByType(query, 'HasValueMult')
      },
      loadMoreListHasValueMult (query) {
        this.loadMoreListByType(query, 'HasValueMult')
      },
      visibleChangeHasValueMult (val) {
        this.currentPageHasValueMult = 1
        if (val) {
          this.resetOptionsList('HasValueMult')
        }
      }
    }
  }
</script>
```
:::

### 创建条目
可以创建并选中选项中不存在的条目
:::demo 使用`allow-create`属性即可通过在输入框中输入文字来创建新的条目。注意此时`filterable`必须为真。本例还使用了`default-first-option`属性，在该属性打开的情况下，按下回车就可以选中当前选项列表中的第一个选项，无需使用鼠标或键盘方向键进行定位。
```html
<template>
  <el-select
    v-model="value10"
    multiple
    filterable
    allow-create
    default-first-option
    placeholder="请选择文章标签">
    <el-option
      v-for="item in options5"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
</template>

<script>
  export default {
    data() {
      return {
        options5: [{
          value: 'HTML',
          label: 'HTML'
        }, {
          value: 'CSS',
          label: 'CSS'
        }, {
          value: 'JavaScript',
          label: 'JavaScript'
        }],
        value10: []
      }
    }
  }
</script>
```
:::

:::tip
如果 Select 的绑定值为对象类型，请务必指定 `value-key` 作为它的唯一性标识。
:::

### Select Attributes 
| 参数      | 说明          | 类型      | 可选值                           | 默认值  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| multiple | 是否多选 | boolean | — | false |
| disabled | 是否禁用 | boolean | — | false |
| value-key | 作为 value 唯一标识的键名，绑定值为对象类型时必填 | string | — | value |
| size | 输入框尺寸 | string | large/medium/small/mini | medium |
| clearable | 单选时是否可以清空选项 | boolean | — | false |
| collapse-tags | 多选时是否将选中值按文字的形式展示 | boolean | — | false |
| multiple-limit | 多选时用户最多可以选择的项目数，为 0 则不限制 | number | — | 0 |
| name | select input 的 name 属性 | string | — | — |
| auto-complete | select input 的 autocomplete 属性 | string | — | off |
| placeholder | 占位符 | string | — | 请选择 |
| filterable | 是否可搜索 | boolean | — | false |
| allow-create | 是否允许用户创建新条目，需配合 `filterable` 使用 | boolean | — | false |
| filter-method | 自定义搜索方法 | function | — | — |
| remote | 是否为远程搜索 | boolean | — | false |
| remote-method | 远程搜索方法 | function | — | — |
| loading | 是否正在从远程获取数据 | boolean | — | false |
| loading-text | 远程加载时显示的文字 | string | — | 加载中 |
| no-match-text | 搜索条件无匹配时显示的文字 | string | — | 无匹配数据 |
| no-data-text | 选项为空时显示的文字 | string | — | 无数据 |
| popper-class | Select 下拉框的类名 | string | — | — |
| reserve-keyword | 多选且可搜索时，是否在选中一个选项后保留当前的搜索关键词 | boolean | — | false |
| default-first-option | 在输入框按下回车，选择第一个匹配项。需配合 `filterable` 或 `remote` 使用 | boolean | - | false |
| popper-append-to-body | 是否将弹出框插入至 body 元素。在弹出框的定位出现问题时，可将该属性设置为 false | boolean | - | true |
| data-for-paper | 是否支持分页加载数据属性 | array | 可选项的数据 | [] |
| page-size | 分页加载，每页加载option条数 | number | - | 50 |
| load-more-text | 加载更多的提示文案 | String | 加载更多 | - |

### Select Events
| 事件名称 | 说明 | 回调参数 |
|---------|---------|---------|
| change | 选中值发生变化时触发 | 目前的选中值 |
| visible-change | 下拉框出现/隐藏时触发 | 出现则为 true，隐藏则为 false |
| remove-tag | 多选模式下移除tag时触发 | 移除的tag值 |
| clear | 可清空的单选模式下用户点击清空按钮时触发 | — |
| blur | 当 input 失去焦点时触发 | (event: Event) |
| focus | 当 input 获得焦点时触发 | (event: Event) |

### Select Slots
|   name  | 说明     |
|---------|---------|
|    —    | Option 组件列表 |
| prefix  | Select 组件头部内容 |

### Option Group Attributes
| 参数      | 说明          | 类型      | 可选值                           | 默认值  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| label | 分组的组名 | string | — | — |
| disabled | 是否将该分组下所有选项置为禁用 | boolean | — | false |

### Option Attributes
| 参数      | 说明          | 类型      | 可选值                           | 默认值  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| value | 选项的值 | string/number/object | — | — |
| label | 选项的标签，若不设置则默认与 `value` 相同 | string/number | — | — |
| disabled | 是否禁用该选项 | boolean | — | false |

### Methods
| 方法名 | 说明 | 参数 |
| ---- | ---- | ---- |
| focus | 使 input 获取焦点 | - |
