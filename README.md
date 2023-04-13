1#SORU - test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.

1#CEVAP - CREATE TABLE employee (
 	id INTEGER PRIMARY KEY,
	name VARCHAR(50) NOT NULL,
	birthday DATE,
	email VARCHAR(100)
);

1#<img width="960" alt="1" src="https://user-images.githubusercontent.com/129968939/231614656-71b13ca4-9476-4927-9f64-9a10988827cf.png">

2#SORU - Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.

2#CEVAP - 

2#<img width="960" alt="2" src="https://user-images.githubusercontent.com/129968939/231615467-48444025-c684-4cd7-8286-6744d959efa4.png">

3#SORU - Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.

3#CEVAP - UPDATE employee
SET name = 'Yılmaz',
	birthday = '2004-04-14',
	email = 'yıl@maz.com'
WHERE name = 'Morgan'
RETURNING*;

3#<img width="960" alt="3" src="https://user-images.githubusercontent.com/129968939/231617074-d967a72d-efd1-46e0-b11a-3be7afd1bdbe.png">

4#SORU - Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.

4#CEVAP - DELETE FROM employee
WHERE name = 'Yılmaz'
RETURNING *;
4#<img width="960" alt="4" src="https://user-images.githubusercontent.com/129968939/231617389-6c031911-15b8-479e-b44a-778ef0d09f4c.png">
