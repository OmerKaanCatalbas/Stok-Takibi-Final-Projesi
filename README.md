# 🧾 StokTakibiFinalProjesi

Java Spring Boot kullanılarak geliştirilmiş basit bir stok takip sistemidir. Ürünleri listeleme, ekleme, silme ve isimle arama gibi temel CRUD işlemleri yapılabilir. PostgreSQL veritabanı kullanılmış ve Railway ile deploy edilmiştir.

---

## 🚀 Kullanılan Teknolojiler

- Java 17  
- Spring Boot 3.5.0  
- Spring Web  
- Spring Data JPA  
- PostgreSQL  
- Railway  
- Maven

---

## 🧱 Katmanlar

| Katman             | Açıklama                                         |
|--------------------|--------------------------------------------------|
| `Product`          | Entity sınıfı                                    |
| `ProductRepository`| JPA için Repository Interface                    |
| `ProductService`   | CRUD iş mantıklarını içerir                      |
| `ProductController`| REST API endpoint'lerini içerir (`/api/products`)|

---

## 📦 API Endpointleri

| Metot   | URL                                | Açıklama                   |
|---------|------------------------------------|----------------------------|
| `GET`   | `/api/products`                    | Tüm ürünleri listeler      |
| `POST`  | `/api/products`                    | Yeni ürün ekler            |
| `DELETE`| `/api/products/{id}`               | ID'ye göre ürünü siler     |
| `GET`   | `/api/products/search?name={isim}` | İsme göre ürün arar        |

---

## 📫 Örnek Postman Kullanımı

### Ürün Silme
```http
DELETE https://<deploy-url>/api/products/1
```

### Ürün Ekleme
```http
POST https://<deploy-url>/api/products
Content-Type: application/json

{
  "name": "Klavye",
  "category": "Donanım",
  "stock": 20,
  "price": 350.0
}
```

### İsimle Arama
```http
GET https://<deploy-url>/api/products/search?name=klavye
```



## 🌐 Deploy Linki

> [https://stok-takibi-final-projesi-production.up.railway.app/](https://stok-takibi-final-projesi-production.up.railway.app/)

---

## 🧑‍💻 Geliştirici

- **Omer Kaan Catalbas**
- Bilgisayar Programcılığı Öğrencisi
