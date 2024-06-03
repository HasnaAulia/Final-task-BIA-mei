![image](https://github.com/HasnaAulia/Final-task-BIA-mei/assets/81562096/b2ad142e-08ec-4bb5-a792-52daf4295258)# [Final Task] Digital User Churn Dashboard

## Challenges 1 (Primary Key)
Menentukan masing-masing primary key pada 4 dataset penjualan
![image](https://github.com/HasnaAulia/Final-task-BIA-mei/assets/81562096/3ee9908e-e995-41c9-b21f-e875c10d35e0)

## Challenges 2 (Table Relationship)
![image](https://github.com/HasnaAulia/Final-task-BIA-mei/assets/81562096/f401e815-5a4a-4cc7-a403-476bead10fca)
- Hubungan one-to-many tabel “ProductCategory” dan “Product”, menunjukkan bahwa satu kategori produk bisa dipilih oleh banyak produk dan sebaliknya, satu produk hanya memiliki satu kategori produk.
- Hubungan one-to-many tabel “Customers” dan “Orders”, menunjukkan bahwa satu customer bisa melakukan banyak order, namun satu order hanya bisa dilakukan oleh satu customer.
- Hubungan one-to-many tabel “Orders” dan “Product”, menunjukkan bahwa setiap Order dapat mencakup banyak Produk, tetapi setiap Produk hanya dapat terkait dengan satu Order.

## Challenges 3 (Membuat Master Table)
```
SELECT
  o.Date AS order_date,
  pc.CategoryName AS category_name,
  p.ProdName AS product_name,
  p.Price AS product_price,
  o.Quantity AS order_qty,
  (p.Price * o.Quantity) AS total_sales,
  c.CustomerEmail AS cust_email,
  c.CustomerCity AS cust_city
FROM
  rakamin.orders o
JOIN
  rakamin.customers c
ON
  o.CustomerID = c.CustomerID
JOIN
  rakamin.product p
ON
  o.ProdNumber = p.ProdNumber
JOIN
  rakamin.productcategory pc
ON
  p.Category = pc.CategoryID
ORDER BY
  order_date ASC;
```

## Challenges 4 (Data Visualization)
Membuat visualisasi dari data pada master table yang sudah dibuat sebelumnya
![image](https://github.com/HasnaAulia/Final-task-BIA-mei/assets/81562096/b4607447-8f18-4aba-b576-4a0fe12b706b)
Dashboard Interaktif dapat dilihat pada [looker studio] (https://lookerstudio.google.com/s/hpwd-FZzkFQ)

## Challenges 5

