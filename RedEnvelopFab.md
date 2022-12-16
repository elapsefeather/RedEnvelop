# RedEnvelope-RedEnvelopFab

紅包浮動提示球 RedEnvelopFab <br>
<img src="./screenshots/sample-EnvelopFab.jpg" height="500">

## Usage 使用方式

1. 需要額外宣吿 addView

```
//  binding
        binding = ActivityMainBinding.inflate(getLayoutInflater());
        setContentView(binding.getRoot());

        fab = new EnvelopeFab(this);
        binding.getRoot().addView(fab);

//  or defValue
        setContentView(layoutResID);

        ↓↓↓↓↓

        ViewGroup viewGroup = (ViewGroup) LayoutInflater.from(this).inflate(layoutResID, null);
        RelativeLayout.LayoutParams params = new RelativeLayout.LayoutParams(LinearLayout.LayoutParams.MATCH_PARENT,
                LinearLayout.LayoutParams.MATCH_PARENT);
        fab = new EnvelopeFab(this)
        viewGroup.addView(fab, params);
        setContentView(viewGroup);
```

2. 需要設置 onConfigurationChanged

```
    @Override
    public void onConfigurationChanged(@NonNull Configuration newConfig) {
        super.onConfigurationChanged(newConfig);
        fab.onConfigurationChanged(newConfig);
    }
```

3. 可以設置相關顯示設置

```
        fab.setImageSize(this, 100);
        fab.setCountBg(getDrawable(R.drawable.fab_bg));
        fab.setOnClickListener(v -> {
            notice();
        });
```

## parameter 可用參數

<table>
    <tr>
        <th>參數名稱</th>
        <th>設置使用型態</th>
        <th>說明</th>
    </tr>
    <tr>
        <td>設置數量</td>
        <td>setCount(int count)</td>
        <td>
            會自動添加 x <br>
            ex: x30
        </td>
    </tr>
    <tr>
        <td>獲取目前數量</td>
        <td>int getCount()</td>
        <td></td>
    </tr>
    <tr>
        <td>設置數量提示字背景</td>
        <td>setCountBg(Drawable)</td>
        <td>padding、margin 已預設完成</td>
    </tr>
    <tr>
        <td>設置數量提示字體大小</td>
        <td>setCountTextSize(float textSize)</td>
        <td></td>
    </tr>
    <tr>
        <td>設置數量提示字體色</td>
        <td>setCountTextColor(int color)</td>
        <td>須先自行轉換可用色彩</td>
    </tr>
    <tr>
        <td>設置移動圖示</td>
        <td>setImage(Drawable drawable)</td>
        <td></td>
    </tr>
    <tr>
        <td>設置移動圖示大小</td>
        <td>setImageSize(Context context, float dpSize)</td>
        <td>
            會依照1:1設置<br>
            dpSize會自行轉換px
        </td>
    </tr>
    <tr>
        <td>浮動球 顯示、隱藏</td>
        <td>show()、hide() </td>
        <td></td>
    </tr>
</table>
