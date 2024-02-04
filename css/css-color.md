## css 边框
#### 实色背景 + 渐变色边框 + 圆角 + 阴影

```
    border-radius: 12px;
    box-shadow: 0px 4px 8px 0px #8F0000 inset;
    border: 2.4px solid transparent;
    border-radius: 10px;
    background-clip: padding-box, border-box;
    background-origin: padding-box, border-box;
    background-image: linear-gradient(to right, #E80021, #E80021),
        linear-gradient(to bottom, rgba(253, 255, 168, 1), rgba(255, 216, 79, 1));
```

## css 字体颜色
#### 文字渐变色 + 阴影
```
.color-text{
    position: relative;
    text-shadow: 2px 4px 4px rgba(189, 4, 11, 1);
    color:#FFD84F;
    font-weight: 700;
    &::after{
        width: 100%;
        position: absolute;
        content: attr(text);
        font-weight: 700;
        left: 50%;
        transform: translateX(-50%);
        color:#FEFFE9;
        -webkit-mask-image:-webkit-gradient(linear, 0 0, 0 100%, from(rgba(0, 0, 0, 0.9)), color-stop(40%, rgba(0, 0, 0, 0.5)), to(rgba(0, 0, 0, 0)));
        text-shadow: 2px 2px 4px rgba(189, 4, 11, 1);
    }
}
```