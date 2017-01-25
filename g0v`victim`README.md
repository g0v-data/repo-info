# 災民證

在災民證為台灣發生災情時，由避難處所負責發放的臨時證件，證件上附有code 128的一維條碼，此專案提供避難處所配合救災或安置需求，解決工作日誌上的業務。

此專案使用 react native 框架開發，目前支援iOS或Android應用。

# 資料格式
```
[
 {
    victimId: '',
    taiwanId: '',
    type: '',
    note: '',
    gps: {
      latitude: 00.00,
      longitude: 00.00,
    },
    createdAt: YYYY-MM-DDThh:mm:ss,
  },
  ...
]
```

# How to run

## Server

### Pre-install
```
npm install -g yarn
```

### Run service
```
yarn install
yarn global add babel-cli
yarn start
```

# License

[MIT License](https://opensource.org/licenses/MIT)