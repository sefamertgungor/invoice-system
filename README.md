# Bitirme Projesi


<details>
  <summary>Proje Gereksinimleri</summary>

- Bir müşteri bilgisi alıp kayıt eden, bir fatura bilgisi kayıt eden ve bu bilgileri sorgulayan restApi ler olacak.
  
- Bir de ödenmiş statüsünde gözüken fatura kaydı oluşturalım. Müşterinin faturası sorgulandığında ödenmemiş faturanın bulunmadığına dair response code ve mesaj dönülsün. (Fatura sorgulama faturaId ve müşteri numarası ile yapılmalı)
  
- Oluşturulan müşteri kaydı ve fatura kaydı için id bilgisi ile silme işlemleri yapan 2 servis olsun.
  
- Fatura kaydı oluşturulacak, kayıt sorgulanabilecek.
  
- Müşteri bilgisi update eden bir servis olacak.

- Bu işlemlerin postgreSql e giden sorgular ile yapacağız. Respository bağlantısı olmalı.
  
- Proje bir maven projesi olacak. Springboot framework ü ile ve SOLID prensiplerine uygun şekilde yazılacak.


  3 adet tablo yeterli. Fatura, User, Payment

  Payment işlemini doğrudan yapılmış gibi hazır kayıt oluşturulması
yeterli.

  Servisler ResponseEntity tipinde cevap dönmeli.
</details>

<details>
  <summary>Rest API Açıklamaları</summary>
  
  - http://localhost:8080/v1/users/save -> It is used in the customer registration section of the system. Name and surname fields should not be blank. Necessary validation procedures have been carried out. 
  - http://localhost:8080/v1/users/get -> Brings all customers registered in the system.
  - http://localhost:8080/v1/users/get/{subscriberId} -> Brings the desired customer with subscriberId.
  - http://localhost:8080/v1/users/delete/{subscriberId} -> Deletes the desired customer with subscriberId.
  - http://localhost:8080/v1/users/update/{subscriberId}?surname=&name= -> Updates the desired customer. (name and surname @RequestParam)
  - http://localhost:8080/v1/invoice/save -> It is used in the invoice registration section of the system. subscriberNo and invoiceAmount fields should not be blank. Necessary validation procedures have been carried out.
  - http://localhost:8080/v1/invoice/get -> Brings all invoices registered in the system.
  - http://localhost:8080/v1/invoice/get/{invoiceNo} -> Brings the desired invoice with invoiceNo.
  - http://localhost:8080/v1/invoice/delete/{invoiceNo} -> Deletes the desired customer with invoiceNo.
  - http://localhost:8080/v1/invoice/invoiceInquiry/{invoiceNo} -> Performs invoice inquiry with invoiceNo.
  
</details>
