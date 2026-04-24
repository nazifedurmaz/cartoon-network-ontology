# cartoon-network-ontology
BBY464
# 🎨 Cartoon Network Ontolojisi

Bu depo, **Cartoon Network** yayın platformunda yayınlanan çizgi filmleri, karakterleri, yaratıcıları ve yapımcı şirketleri modelleyen bir OWL ontolojisi içermektedir. Ontoloji Protégé 5.x ortamında geliştirilmiş olup üç farklı formatta sunulmaktadır.

---

## 📁 Depo Yapısı

```
cartoon-network-ontology/
├── ontology/
│   ├── cartoon-network.owl   ← Ana OWL/XML dosyası (Protégé ile açılır)
│   ├── cartoon-network.rdf   ← RDF/XML formatı
│   └── cartoon-network.ttl   ← Turtle (TTL) formatı
├── terms.txt                 ← Tüm terimler, tanımlar ve bireyler listesi
└── README.md                 ← Bu dosya
```

---

## 🧠 Ontoloji Hakkında

**Protégé Proje Adı:** `CartoonNetworkOntology`  
**Namespace:** `http://www.semanticweb.org/ontologies/2024/cartoonnetwork#`  
**Versiyon:** 1.0.0  
**Dil:** OWL 2 (Web Ontology Language)

Bu ontoloji şu alanları kapsamaktadır:

- Cartoon Network çizgi filmlerinin türlere göre sınıflandırılması
- Çizgi film karakterlerinin rollere göre modellenmesi (Kahraman, Kötü Adam, Yan Karakter)
- Karakterler arasındaki sosyal ilişkiler (arkadaşlık, düşmanlık)
- Yapımcı şirketler ve yaratıcılar
- Sezon ve bölüm sayısı, yayın yılı gibi veri özellikleri

---

## 🗂️ Sınıf Hiyerarşisi

```
ÇizgiFilm
  ├── AksiyonÇizgiFilmi
  ├── KomediÇizgiFilmi
  ├── BilimKurguÇizgiFilmi
  └── FanteziÇizgiFilmi

Karakter
  ├── Kahraman
  ├── KötüAdam
  └── YanKarakter

YapımcıŞirket
Yaratıcı
Sezon
Bölüm
```

---

## 📺 Kapsanan Çizgi Filmler

| Çizgi Film | Tür | Yayın Yılları | Sezon |
|---|---|---|---|
| Adventure Time | Fantezi | 2010–2018 | 10 |
| Steven Universe | Aksiyon | 2013–2019 | 5 |
| Samurai Jack | Aksiyon | 2001–2017 | 5 |
| The Powerpuff Girls | Aksiyon | 1998–2005 | 6 |
| Dexter's Laboratory | Komedi | 1996–2003 | 4 |
| Ben 10 | Bilim Kurgu | 2005–2008 | 4 |
| Regular Show | Komedi | 2010–2017 | 8 |
| Courage the Cowardly Dog | Komedi | 1999–2002 | 4 |

---

## 🔗 İlişkiler (Object Properties)

| Özellik | Alan | Aralık | Açıklama |
|---|---|---|---|
| `karakteriVar` | ÇizgiFilm | Karakter | Film ile karakter arasındaki bağ |
| `tarafındanYaratıldı` | ÇizgiFilm | Yaratıcı | Filmin yaratıcısı |
| `tarafındanYapıldı` | ÇizgiFilm | YapımcıŞirket | Filmin yapımcısı |
| `arkadaşı` | Karakter | Karakter | Simetrik dostluk ilişkisi |
| `düşmanı` | Karakter | Karakter | Simetrik düşmanlık ilişkisi |
| `sezoniçerir` | ÇizgiFilm | Sezon | Film–sezon bağlantısı |
| `bölümiçerir` | Sezon | Bölüm | Sezon–bölüm bağlantısı |

---

## 📊 Veri Özellikleri (Data Properties)

| Özellik | Tip | Açıklama |
|---|---|---|
| `yayınYılı` | xsd:integer | İlk yayın yılı |
| `bitişYılı` | xsd:integer | Son yayın yılı |
| `sezonSayısı` | xsd:integer | Toplam sezon sayısı |
| `bölümSayısı` | xsd:integer | Toplam bölüm sayısı |
| `isim` | xsd:string | Karakter adı |
| `ülke` | xsd:string | Yapımcı şirketin ülkesi |

---

## 🚀 Protégé ile Nasıl Açılır?

1. [Protégé 5.x](https://protege.stanford.edu/) uygulamasını indirin ve açın.
2. `File → Open` menüsünden `cartoon-network.owl` dosyasını seçin.
3. **Classes** sekmesinden sınıf hiyerarşisini inceleyin.
4. **Object Properties** ve **Data Properties** sekmelerinden ilişkileri görüntüleyin.
5. **Individuals** sekmesinden tüm çizgi film ve karakter bireylerini görün.
6. **Reasoner → Start Reasoner (HermiT)** ile çıkarım yapabilirsiniz.

---

## 🛠️ Teknik Detaylar

- **Geliştirme Aracı:** Protégé 5.6.x
- **OWL Profili:** OWL 2 DL
- **Reasoner:** HermiT 1.4.x
- **Encoding:** UTF-8
- **Dil Etiketleri:** Türkçe (`@tr`) ve İngilizce (`@en`)

---

## 👤 Proje Bilgisi

Bu ontoloji, bilgi temsili ve ontoloji mühendisliği dersi kapsamında geliştirilmiştir.

