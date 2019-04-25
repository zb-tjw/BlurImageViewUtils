# BlurImageView
Android ImageView实现高斯模糊的工具类
<h1>具体使用</h1>
<p>1.在GitHub上找了两个相关的库，但是并不好用，首先模糊度不好去调整，其次图片不能设置缩放，如果是wrap_content，则图片可能会有大部分留白，
很难看，我想到的解决办法是设置ScaleX和ScaleY属性，但是效果并不好，而且不支持imageview的src等属性</p>
<p>2.自己修改模糊度也可使用工具类里默认写好的</p>

```
/** 水平方向模糊度 */
    public static final float HRADIUS = 5;
    /** 竖直方向模糊度 */
    public static final float VRADIUS = 5;
    /** 模糊迭代度 */
    public static final int ITERATIONS = 5;
```
<p>3.然后在需要的ImageView上直接调用BoxBlurFilter()方法传入一个bitmap即可，可以通过scaleType属性指定缩放</p>

```
imgTest.setBackground(BoxBlurFilter(bitmap));
```
4.效果展示<br/>
<img src="https://github.com/zb-tjw/BlurImageView/blob/master/Screenshot_2019-04-25-22-16-34-136_bzu.zb_tjw.bzu.png" width="480" height="600" alt="效果展示图"/>
<img src="https://github.com/zb-tjw/BlurImageView/blob/master/Screenshot_2019-04-25-22-16-50-708_bzu.zb_tjw.bzu.png" width="480" height="600" alt="效果展示图"/>
