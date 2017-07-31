# API
## API Get Products

API Get Products เป็น API ที่ให้บริการในการดึงค่าข้อมูลต่างๆ ของสินค้าทั้งหมดที่มีในระบบ เช่น รหัสสินค้า ชื่อสินค้า เป็นต้น

### API Call

```
[GET] https://api.sellsuki.com/public/{SELLSUKI_KEY}/products
```

### Attribute

* #### Attribute Product

| **Name** | **Description** |
| :--- | :--- |
| id | id ของ product นั้น โดยจะเป็นการ  running number |
| code\_temp | รหัสสินค้าที่ระบบของ Sellsuki ทำการ Generate ให้อัตโนมัติ |
| name | ชื่อสินค้า |
| description | คำอธิบายของสินค้า |
| status | สถานะของสินค้า \(0 - delete , 1 - active\) |
| store\_id | id ของร้านค้า |
| variant\_1 , variant\_2 , variant\_3 | เก็บ variant ของสินค้าเช่น size,color หากไม่กำหนดจะเก็บข้อมูลเป็น SKU ที่ variant\_1 |
| warehouse\_name | ชื่อของ warehouse |
| photos | รูปภาพของสินค้า \(array\) |

* #### Attribute Product SKU

| **Name** | **Description** |
| :--- | :--- |
| id | id ของ product\_sku เป็นการ running number |
| option1 , option2 , option3 | ข้อมูลที่ตัดมาจาก option\_concat\_1 , option\_concat\_2 , option\_concat\_3 |
| code | รหัสสินค้าที่ร้านค้ากำหนดขึ้นเอง |
| price | ราคาของสินค้า |
| status | สถานะของสินค้า \(0 - delete , 1 - active\) |
| product\_id | รหัสของสินค้า จากตาราง Product |
| stock | จำนวนคงเหลือใน Stack |
| src | รูปภาพของสินค้า |

### Json

```js
results: [
{
    id: "110001",
    code_temp: "PD00020",
    name: "EMS",
    description: "",
    status: "1",
    create_by_sellsuki_user_id: "9554",
    update_by_sellsuki_user_id: "9554",
    create_time: "2017-05-22 10:18:26",
    update_time: "2017-05-22 10:18:26",
    variant_1: "Size",
    variant_2: "",
    variant_3: "",
    gen_url: "",
    product_tags: null,
    concat_lot_type_all_warehouse: "normal:;:normal:;:normal",
    concat_warehouse_name_all_warehouse: "sellsuki:;:sellsuki:;:sellsuki",
    concat_remaining_quantity_all_warehouse: "10:;:10:;:10",
    concat_sku_cost: "200.00:;:200.00:;:200.00",
    warehouse_name: "sellsuki",
    product_brand: null,
    product_src: "https://sellsuki-picture.s3-ap-southeast-1.amazonaws.com/kQDKQCsKKx420150731T0523S2318740056711316220.png",
    concat_product_category: null,
    concat_product_tag: null,
    concat_product_shelf: null,
    photos: [
    "https://sellsuki-picture.s3-ap-southeast-1.amazonaws.com/kQDKQCsKKx420150731T0523S2318740056711316220.png"
    ],
    skus: [
    {
        id: "796514",
        option1: "s",
        option2: "",
        option3: "",
        code: "PD00020-1",
        price: "250.00",
        status: "1",
        stock: "10",
        src: "https://sellsuki-picture.s3-ap-southeast-1.amazonaws.com/kQDKQCsKKx420150731T0523S2318740056711316220.png"
    },
    {
        id: "796515",
        option1: "m",
        option2: "",
        option3: "",
        code: "PD00020-2",
        price: "250.00",
        status: "1",
        stock: "10",
        src: ""
    },
    {
        id: "796516",
        option1: "l",
        option2: "",
        option3: "",
        code: "PD00020-3",
        price: "250.00",
        status: "1",
        stock: "10",
        src: ""
    }
    ]
},
```




## API Get Product

API Get Product เป็น API ที่ให้บริการในการดึงค่าข้อมูลต่างๆ ของสินค้าแต่ละชิ้นในระบบ เช่น รหัสสินค้า ชื่อสินค้า เป็นต้น

### API Call

```
[GET] https://api.sellsuki.com/public/{SELLSUKI_KEY}/products/{id}
```

### Attribute

* #### Attribute Product

| **Name** | **Description** |
| :--- | :--- |
| id | id ของ product นั้น โดยจะเป็นการ  running number |
| code\_temp | รหัสสินค้าที่ระบบของ Sellsuki ทำการ Generate ให้อัตโนมัติ |
| name | ชื่อสินค้า |
| description | คำอธิบายของสินค้า |
| status | สถานะของสินค้า \(0 - delete , 1 - active\) |
| store\_id | id ของร้านค้า |
| variant\_1 , variant\_2 , variant\_3 | เก็บ variant ของสินค้าเช่น size,color หากไม่กำหนดจะเก็บข้อมูลเป็น SKU ที่ variant\_1 |
| warehouse\_name | ชื่อของ warehouse |
| photos | รูปภาพของสินค้า \(array\) |

* #### Attribute Product SKU

| **Name** | **Description** |
| :--- | :--- |
| id | id ของ product\_sku เป็นการ running number |
| option1 , option2 , option3 | ข้อมูลที่ตัดมาจาก option\_concat\_1 , option\_concat\_2 , option\_concat\_3 |
| code | รหัสสินค้าที่ร้านค้ากำหนดขึ้นเอง |
| price | ราคาของสินค้า |
| status | สถานะของสินค้า \(0 - delete , 1 - active\) |
| product\_id | รหัสของสินค้า จากตาราง Product |
| stock | จำนวนคงเหลือใน Stack |
| src | รูปภาพของสินค้า |

### Json

```js
results: [
{
    id: "399804",
    code_temp: "PD00020",
    name: "EMS",
    description: "",
    status: "1",
    create_by_sellsuki_user_id: "9554",
    update_by_sellsuki_user_id: "9554",
    create_time: "2017-05-22 10:18:26",
    update_time: "2017-05-22 10:18:26",
    variant_1: "Size",
    variant_2: "",
    variant_3: "",
    gen_url: "",
    product_brand: null,
    product_tags: null,
    product_src: "https://sellsuki-picture.s3-ap-southeast-1.amazonaws.com/kQDKQCsKKx420150731T0523S2318740056711316220.png",
    photos: [
    "https://sellsuki-picture.s3-ap-southeast-1.amazonaws.com/kQDKQCsKKx420150731T0523S2318740056711316220.png"
    ],
    skus: [
    {
        id: "796514",
        option1: "s",
        option2: "",
        option3: "",
        code: "PD00020-1",
        price: "250.00",
        status: "1",
        stock: "10",
        src: "https://sellsuki-picture.s3-ap-southeast-1.amazonaws.com/kQDKQCsKKx420150731T0523S2318740056711316220.png"
    },
    {
        id: "796515",
        option1: "m",
        option2: "",
        option3: "",
        code: "PD00020-2",
        price: "250.00",
        status: "1",
        stock: "10",
        src: ""
    },
    {
        id: "796516",
        option1: "l",
        option2: "",
        option3: "",
        code: "PD00020-3",
        price: "250.00",
        status: "1",
        stock: "10",
        src: ""
    }
    ]
}
]
```

## API Create Order 


API Create Order เป็น API ที่ให้บริการในการสร้าง Order ของการสั่งซื้อสินค้า โดยสามารถใช้งาน API นี้ได้ตั้งแต่ขั้นตอนแรกของการสร้าง Order

### API Call

```
[POST] https://api.sellsuki.com/public/{SELLSUKI_KEY}/submit
```

### Attribute

| **Name** | **Description** |
| :--- | :--- |
| skus | array ที่เก็บข้อมูลของสินค้าแต่ละ sku |
| skus\[0\]\[id\] | id ของ sku |
| skus\[0\]\[price\] | ราคาของสินค้า |
| skus\[0\]\[amount\] | จำนวนของสินค้า |
| skus\[0\]\[name\] | ชื่อสินค้า |
| skus\[0\]\[option1 , option2 , option3\] | รายละเอียดย่อยของสินค้า \(ถ้ามี\) |
| skus\[0\]\[warehouse\] | warehouse ที่สินค้าอยู่ |
| email | email ของลูกค้า |
| tel | หมายเลขโทรศัพท์ของลูกค้า |
| shipping\_type | ประเภทของการจัดส่ง |
| shipping\_price | ค่าจัดส่ง |
| pay\_order | \(Default value is 1.\) |
| debt\_balance | ยอดชำระของบิล |

### Json

```js
{
    "skus": [{
        "id": "46484",
        "price": "100",
        "amount": "1",
        "name": "หมา",
        "option1": "1",
        "option2": "2",
        "option3": "3",
        "warehouse": "sellsuki"
    }],
    "email": "",
    "tel": "",
    "shipping_type": "-",
    "shipping_price": 0,
    "debts": [{
        "pay_order": 1,
        "debt_balance": 100
    }]
}
```



## API Update Order 

(in Progess)

## API Prepare to Ship

API Prepare to Ship เป็น API ที่ให้บริการในการดึงค่าข้อมูลต่างๆ ที่สถานะอยู่ในขั้นตอนของการเตรียมจัดส่ง

### API Call

```
[POST] https://api.sellsuki.com/public/{SELLSUKI_KEY}/prepare-bill
```

### Attribute

| **Name** | **Description** |
| :--- | :--- |
| bill\_id | เป็นเลข ID ของ Bill |

### Parameter Json

```js
{
	"bill_id": "O0117AERVDER00001"
}
```

โดยจะได้รับค่าส่งคืนกลับมา

* success

```
"result":[{"success":1}]}
```

* failed

```
"result":[{"success":0}]}
```

## API Deduct Stock

API Deduct Stock เป็น API ที่ให้บริการในการดึงค่าข้อมูลต่างๆ ที่สถานะอยู่ในขั้นตอนของการตัดสต๊อค

### API Call

```
[POST] https://api.sellsuki.com/public/{SELLSUKI_KEY}/deduct-bill
```

### Attribute

| **Name** | **Description** |
| :--- | :--- |
| bill\_id | เป็นเลข ID ของ Bill |

### Parameter Json

```js
{
	"bill_id": "O0117AERVDER00001"
}
```

โดยจะได้รับค่าส่งคืนกลับมา

* success

```
"result":[{"success":1}]}
```

* failed

```
"result":[{"success":0}]}
```



## API Shipping

API Shipping เป็น API ที่ให้บริการในการดึงค่าข้อมูลต่างๆ ที่สถานะอยู่ในขั้นตอนของการจัดส่ง

### API Call

```
[POST] https://api.sellsuki.com/public/{SELLSUKI_KEY}/shipping-bill
```

### Attribute

| **Name** | **Description** |
| :--- | :--- |
| bill\_id | เป็นเลข ID ของ Bill |
| tracking\_number \(Optional\) | เลข Tracking Number ของพัสดุที่จัดส่ง |

### Parameter Json

```js
{
	"bill_id": "O0117AERVDER00001",
	"logistic_refcode": "AA1234567890TH"
}
```

โดยจะได้รับค่าส่งคืนกลับมา

* success

```
"result":[{"success":1}]}
```

* failed

```
"result":[{"success":0}]}
```






<br><br><br><br><br><br><br>





