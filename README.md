# API Test Case-ləri

---

## Test Case 1: Düzgün Məlumatlarla POST Sorğusunun Yoxlanılması

### Description
Düzgün məlumatlarla yeni qeyd yaratmağın mümkün olduğunu yoxlamaq.

### Pre-condition
- API aktivdir.

### Test Steps
1. POST metodunu seçirik.
2. URL-ni daxil edirik.
3. Body hissəsinə düzgün JSON məlumatı əlavə edirik.
4. Sorğunu göndəririk.

### Expected Result
- Status Code: 201 Created
- Yeni qeyd yaradılır
- Cavabda yaradılmış qeyd qaytarılır

---

## Test Case 2: Mövcud Qeyd Üzərində Update Əməliyyatının Yoxlanılması

### Description
PUT sorğusu vasitəsilə mövcud məlumatın yenilənməsini yoxlamaq.

### Pre-condition
- Sistemdə mövcud qeyd var.
- Qeyd ID-si məlumdur.

### Test Steps
1. PUT metodunu seçirik.
2. Endpoint URL-də mövcud ID-ni daxil edirik.
3. Yenilənəcək məlumatları daxil edirik.
4. Sorğunu göndəririk.

### Expected Result
- Status Code: 200 OK
- Məlumat uğurla yenilənir

---

## Test Case 3: Mövcud Qeyd Silinməsinin Yoxlanılması

### Description
DELETE sorğusu vasitəsilə məlumatın silinməsini yoxlamaq.

### Pre-condition
- Sistemdə silinə biləcək ID mövcuddur.

### Test Steps
1. DELETE metodunu seçirik.
2. Mövcud ID ilə sorğu göndəririk.

### Expected Result
- Status Code: 200 OK
- Qeyd sistemdən silinir

---

## Test Case 4: Boş Body ilə POST Sorğusu

### Description
POST sorğusunda body hissəsi boş olduqda sistemin xəta qaytarmasını yoxlamaq.

### Pre-condition
- API aktivdir.

### Test Steps
1. Body hissəsini boş saxlayın.
2. POST sorğusu göndərin.

### Expected Result
- Status Code: 400 Bad Request
- Validation error qaytarılır

---

## Test Case 5: Mövcud Olmayan ID ilə Sorğu

### Description
Mövcud olmayan ID göndərildikdə sistemin düzgün cavab verdiyini yoxlamaq.

### Pre-condition
- Sistemdə olmayan ID mövcuddur.

### Test Steps
1. GET sorğusunu yanlış ID ilə göndərin.

### Expected Result
- Status Code: 404 Not Found
- Record tapılmadı mesajı qaytarılır
