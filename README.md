# ToDoApp4 

## Özellikler

- Görev ekleme
- Görev tamamlama ve geri alma
- Görev silme
- Liste halinde görevleri görüntüleme
- State yönetimi (StateFlow)
- Temel Compose UI kullanımı

---

## Kullanılan Teknolojiler

- **Kotlin**
- **Jetpack Compose**
- **StateFlow**
- **MVVM Mimarisi**
- **Material3**

---

## Karşılaşılan Hatalar ve Çözümleri

### 1. Proje Adı Uyuşmazlığı (Manifest Hatası)
- **Sorun:** `AndroidManifest.xml` içindeki `package` adı proje dosyasıyla uyuşmuyordu.
- **Çözüm:** Dosyadaki `package` tanımı `com.example.todoapp4` olarak güncellendi.

### 2. MainActivity'de Import Eksikliği
- **Sorun:** `setContent` ve `MaterialTheme` fonksiyonları için gerekli import'lar eksikti.
- **Çözüm:** `import androidx.activity.compose.setContent` ve `import androidx.compose.material3.MaterialTheme` satırları eklendi.

### 3. UI Dosyalarının Yanlış Konumu
- **Sorun:** `TodoScreen.kt` dosyası `ui/` klasörü dışında konumlandırılmıştı.
- **Çözüm:** Uygun klasöre taşındı ve `package` ismi düzeltildi.

### 4. ViewModel Doğrudan Oluşturuluyordu (OOP Hatası)
- **Sorun:** ViewModel doğrudan `TodoViewModel()` şeklinde oluşturuluyordu.
- **Çözüm:** `by viewModels()` şeklinde yaşam döngüsüne duyarlı olarak kullanılmalıydı.

### 5. `copy()` Kullanımıyla İlgili Syntax Riski
- **Sorun:** `copy()` fonksiyonu doğru kullanılamadığında IDE'de hata verir.
- **Çözüm:** `copy(isDone = !it.isDone)` şeklinde doğru kullanıldı.

---

## Öğrendiklerim

- Jetpack Compose ile arayüz geliştirme
- MVVM mimarisi uygulama
- Kotlin’de `StateFlow` ile reaktif veri yönetimi
- Hata ayıklama ve çözüme ulaşma süreci


