# Get Started

Docs นี้จะช่วยคุณในการนำ Plug-in ของ Sellsuki ไปใช้บน Wordpress ร้านค้าของคุณ โดยคุณสามารถทำตามขั้นตอนด้านล่างนี้ได้แบบ Step by Step

##### การติดตั้ง Plug-in บน Wordpress

เข้าไปที่ Wordpress ของคุณ แล้วเข้าไปที่เมนู "**ปลั๊กอิน**" หลังจากนั้นให้คลิกที่เมนู "**เพิ่มปลั๊กอินใหม่**"

![](/assets/import4.png)

หลังจากนั้นคลิกที่ "**อัพโหลดปลั๊กอิน**"

![](/assets/import5.png)

หลังจากนั้น ให้คลิก "**เลือกไฟล์**" แล้วอัพโหลดไฟล์ sellsuki-shop.zip แล้วคลิก "**ติดตั้งเดี๋ยวนี้**"

![](/assets/import3.png)

หลังจากติดตั้ง Plug-in  เสร็จเรียบร้อยแล้ว ให้คลิกที่ "**ใช้งานปลั๊กอิน**"

![](/assets/import6.png)

เมื่อทำการติดตั้งปลั๊กอินแล้ว จะพบว่ามีปลั๊กอินของ Sellsuki เข้ามาใน Side Bar ด้านซ้ายมือ ต่อจากนี้จะทำการตั้งค่า \(Setting\) ปลั๊กอินที่ติดตั้ง โดยไปที่เมนู "**Sellsuki Plugin**" --&gt; **Setting**

![](/assets/import7.png)

เมื่อเข้าสู่หน้า Setting แล้ว ให้เรานำ Sellsuki Key ที่ได้จากระบบของ Sellsuki \(ในเมนู **ตั้งค่า **--&gt; **ตั้งค่า Plugin ตะกร้าหน้าร้าน \(Beta\)** \) มาใส่ใน Textbox

![](/assets/import8.png)![](/assets/import10.png)

เมื่อใส่ Sellsuki Key เรียบร้อยแล้ว ให้ คลิกที่ "**Advance Setting**" เพื่อเลือก Post Type เป็น **WooCommerce **\(ต้องติดตั้ง WooCommerce ก่อน ถึงจะมีตัวเลือกของ WooCommerce\)

![](/assets/import11.png)



# Add Product

Add Product คือการเพิ่มสินค้า จากระบบของ Sellsuki เข้าระบบของผู้ใช้ใน Wordpress โดยการใช้งาน Add Product นี้ จะต้องผ่านการติดตั้ง Plug-in ของ Sellsuki และใส่ Sellsuki Key เรียบร้อยแล้ว วิธีการ Add Product มีขั้นตอนดังนี้

ขั้นแรกให้เข้าไปที่ Sellsuki Plugin แล้วเลือก "**Product Page**" จากนั้น เลือกสินค้าที่ต้องการเพิ่มในร้านค้าของผู้ใช้ โดยคลิก "**Add Product**"

![](/assets/import12.png)

จากนั้นปุ่ม "Add Product" จะเปลี่ยนเป็น "Update Product" ซึ่งถ้าเราคลิกที่ "**Update Product**" สินค้านั้นจะถูกนำเข้าร้านค้าของผู้ใช้ใน Wordpress ทันที

![](/assets/import13.png)

เราสามารถเช็คข้อมูลสินค้าที่เรานำเข้าระบบ Wordpress ได้โดยไปที่เมนู "**สินค้า**" จะพบว่ามีสินค้าเข้ามาในระบบแล้ว

![](/assets/import14.png)

### แก้ไขสินค้า

ในกรณีที่เราต้องการแก้ไขรายละเอียดต่างๆ ของสินค้า หรือต้องการดึงข้อมูลบางอย่าง โดยให้มีการอัพเดตอัตโนมัติ เมื่อข้อมูลสินค้าในระบบของ Sellsuki มีการเปลี่ยนแปลง เราสามารถทำได้โดยวิธีดังนี้

ขั้นแรกให้เข้าไปที่เมนู "**แก้ไขสินค้า**" ใน Wordpress

![](/assets/import15.png)

เราสามารถพิมพ์ข้อความรายละเอียดของสินค้าได้ตามที่ต้องการ 

แต่ถ้าต้องการให้ดึงข้อมูลมาจากระบบของ Sellsuki แบบอัตโนมัติ สามารถทำได้ 3 อย่างคือ  

* ราคาสินค้า

```
[sskbtnprice]
```

* ปุ่มกดสั่งซื้อสินค้า

```
[sskbtnbuy]
```

* ตัวเลือก SKU ของสินค้า

```
[sskvariant]
```



### การสร้างตะกร้าสินค้าบน Website

ผู้ใช้สามารถสร้างตะกร้าสินค้าบน Website ได้โดยนำโค้ดด้านล่างใส่ไว้ในตำแหน่งที่ต้องการให้มีตะกร้าสินค้าปรากฎ

```html
<div class="ssk-cart-wrap">
    <button id="sellsuki-cart"
class="sellsuki-button--cart">
        <i class="sellsuki-open-carticon"></>
        <span id="sellsuki-notification"
class="sellsuki-button--
cart__noti">{price}</span>
    </button>

</div>
```

<br><br><br><br><br><br><br><br><br><br>



