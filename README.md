## วิธีใช้ 

1. ติดตั้ง addon ด้วยการ add repository : https://github.com/racksync/hass-addons-autossh-tunnel เข้าไปยัง addon list ตามปกติ
2. ตั้งค่า hostname / user / remote_forwarding ปลายทางให้ครบถ้วน
3. start adddon แล้วเข้าไปยัง logs tab ของ addon เพื่อก๊อปปี้ public key ไปยัง ~/.ssh/authorized_keys
4. restart addon อีกครั้ง

```
hostname: '[SERVER-ADDRESS]'
ssh_port: 22
username: root
remote_forwarding:
  - 127.0.0.1:8123:192.168.0.10:8123
other_ssh_options: '-v'
force_keygen: false
```
## ข้อควรระวัง

- บน production ไม่ควร login ด้วย root
- ไม่ควร expose port ไปที่ 0.0.0.0 หรือ public address (ควรใช้ร่วมกับ reverse proxy) 

## หากพบปัญหาในการใช้งาน กรุณาส่งเข้า issue

### บริการและเทรนนิ่งคอร์สด้าน Automation 

- [สินค้าและบริการ](https://racksync.com)
- [เทรนนิ่งคอร์ส](https://facebook.com/racksync)

### ชุมชนและแหล่งซื้อขาย Home Automation

- [Home Automation Thailand](https://www.facebook.com/groups/hathailand)
- [Home Automation Marketplace](https://www.facebook.com/groups/hatmarketplace)
