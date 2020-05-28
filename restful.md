Multi-Coin Crypto-Payment Gateway provides a simple and robust RESTful API to integrate digital currency payment gateway with your application

The Multi-Coin Crypto-Payment Gateway enables the following:

- Get select coin with rates
- Create invoice
- Get invoice data


Get listed supported coin with rates (Multi-coin payment only)

```
http://mywebsite.com/api.php?coins&amount=50

```

Request samples (application/json)

```JSON
[
    {
        "coin": "btc",
        "name": "Bitcoin",
        "rate": 0.00527449,
        "coin_logo": "assets\/img\/btc.png"
    },
    {
        "coin": "bch",
        "name": "Bitcoin Cash",
        "rate": 0.20802564,
        "coin_logo": "assets\/img\/bch.png"
    },
    {
        "coin": "ltc",
        "name": "Litecoin",
        "rate": 1.1350312,
        "coin_logo": "assets\/img\/ltc.png"
    },
    {
        "coin": "dash",
        "name": "Dash",
        "rate": 0.64720408,
        "coin_logo": "assets\/img\/dash.png"
    },
    {
        "coin": "zec",
        "name": "Zcash",
        "rate": 1.04373189,
        "coin_logo": "assets\/img\/zec.png"
    }
]

```


Create new payment invoice API Link Example (Create New payment)

```
http://mywebsite.com/api.php?amount=50&coin=btc

```

Request samples (application/json)

```JSON

{
    "id": "5ec5ef865924a",
    "user_id": "5ec5ef865924d",
    "invoice": "f9UTEpRKeSKe",
    "payment_id": "vReb4Wb0R2rfSeT",
    "amount": "0.00527449",
    "address": "3AWRiFuy7iWTPSaocWJ314jiTtkjQCuW4j",
    "dollar": 50.5,
    "expiring": 43200000,
    "coin": "ZEC",
    "coin_logo": "assets\/img\/zec.png",
    "fees": "0.5",
    "qrcode": "https:\/\/chart.googleapis.com\/chart?chs=500x500&cht=qr&chl=bitcoin:3AWRiFuy7iWTPSaocWJ314jiTtkjQCuW4j&choe=UTF-8",
    "qramount": "https:\/\/chart.googleapis.com\/chart?chs=500x500&cht=qr&chl=amount=0.00527449&choe=UTF-8",
    "created": "1 sec ago",
    "status": 1
}


```


Get invoice data using the invoice id API Link Example

```
http://mywebsite.com/api.php?invoice=Pde00C23eCST

```


Request samples (application/json)

```JSON
{
"id":"168",
"user_id":"2147483647",
"invoice":"9naRlgyKVmQN",
"payment_id":"8OYLEWGpmGJufaZ",
"amount":"0.00039289",
"dollar":"2",
"address":"2Mxvs5M6DaCswJkrFCz3pRxL5W23gNzQ2Vw",
"coin":"tbtc",
"payment_type":"product",
"txt":"c64aa36121e21e1b2a33059a75cf4a59294d2dc1dcb210c7b69f19325800b161",
"date_confirmed":"0000-00-00 00:00:00",
"invoice_time":"43200",
"paid":"0",
"created":"2020-03-18 17:13:41",
"status":1
}

```


<br>
<br>