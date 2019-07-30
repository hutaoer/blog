# antd使用tips

## 给 Switch 设置默认值
```html
<FormItem label='在搜索结果中屏蔽'>
    {
        getFieldDecorator('checked', {
            initialValue: this.props.checked,
            valuePropName: 'checked'
        })(<Switch />)
    }
</FormItem>
```