# RTX1200の学習メモ

## その他

### PWの初期化

1. PCとRTX1200をケーブルで接続
2. 例として、TeraTermにて、「シリアル」でポート「COMn: Dtech USB Serial Controller (COMn)」を指定し、「OK」
3. 真っ暗な画面で[Enter]
4. 「Password:」と表示後、(シリアルのみ)下記を入力し、[Enter][^1]
   ```
   w,lXlma
   ```
5. 「＃R1」が表示されれば、管理者モードでログイン成功
6. 下記を実行
   ```
   # login password
   Old_Password: w,lXlma
   New_Password: **********
   New_Password: **********
   # administrator password
   Old_Password: w,lXlma
   New_Password: **********
   New_Password: **********
   save
   ```

### コンソールの文字化けの対処

- TeraTermの設定
  1. 「設定 > 端末」を選択
  2. 「漢字-受信」と「漢字-送信」の設定を「SJIS」に変更
- YAMAHAの設定 ？？？
  - ログイン後、下記を入力 [^2]
    ```
    R1# console character ja.utf8
    エラー: パラメータのキーワードが認識できません
    ```
    なお、TeraTermの初期値に合わせる場合「ja.utf8」となる

[^1]: https://www.rtpro.yamaha.co.jp/RT/manual/rt-common/setup/security_class.html
[^2]: https://www.rtpro.yamaha.co.jp/RT/manual/rt-common/setup/console_character.html

## 参考資料

- [GitHub Docs - 基本的な書き方とフォーマットの構文](https://docs.github.com/ja/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

