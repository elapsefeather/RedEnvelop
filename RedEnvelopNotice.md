# RedEnvelope-RedEnvelopNotice

領取紅包提示效果 RedEnvelopNotice <br>
<img src="./screenshots/sample-EnvelopNotice.jpg" height="500">

## Usage 使用方式

```
        EnvelopNotice notice = new EnvelopNotice.Builder(this)
                .setFromName("Mini")
                .setFromEnd("送彩金！")
                .setMoney(money.toString())
                .setNoticeListener(dialog -> {
                    dialog.dismiss();
                    setList(false, envelopData);
                })
                .show();
```

## parameter 可用參數

<table>
    <tr>
        <th>參數名稱</th>
        <th>設置使用型態</th>
        <th>說明</th>
    </tr>
    <tr>
        <td>發送人名稱</td>
        <td>setFromName(CharSequence)</td>
        <td>
            ex:<br>
            [FromStart][FromName][FromEnd]<br>
            [感謝][Mini][送彩金！]
        </td>
    </tr>
    <tr>
        <td>發送人前綴</td>
        <td>setFromStart(CharSequence)</td>
        <td>
            ex:<br>
            [FromStart][FromName][FromEnd]<br>
            [感謝][Mini][送彩金！]
        </td>
    </tr>
    <tr>
        <td>發送人後綴</td>
        <td>setFromEnd(CharSequence)</td>
        <td>
            ex:<br>
            [FromStart][FromName][FromEnd]<br>
            [感謝][Mini][送彩金！]
        </td>
    </tr>
    <tr>
        <td>領取金額前綴</td>
        <td>setGetT(CharSequence)</td>
        <td></td>
    </tr>
    <tr>
        <td>顯示金額</td>
        <td>setMoney(CharSequence)</td>
        <td></td>
    </tr>
    <tr>
        <td>領取按鈕顯示字</td>
        <td>setGiveT(CharSequence)</td>
        <td></td>
    </tr>
    <tr>
        <td>領取按鈕監聽</td>
        <td>setNoticeListener(NoticeListener)</td>
        <td></td>
    </tr>
    <tr>
        <td>可否空白處關閉</td>
        <td>setCancelable(Boolean)</td>
        <td></td>
    </tr>
    <tr>
        <td>關閉監聽</td>
        <td>setOnDismissListener(DialogInterface.OnDismissListener)</td>
        <td></td>
    </tr>
</table>
