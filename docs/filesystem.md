# postgresql dizin yapısı
Paketten varsayılan olarak kurulumda:
```
Çalıştırılabilirler : /usr/pgsql-${version}/bin
Kütüphaneler      : /usr/pgsql-${version}/lib
Yapılandırma (config) dosyaları ve veri  : /var/lib/pgsql/${version}/data
```

## data altındaki yeni başlayanlar için önemli dosyalar ve dizinler
| dosya adı | görevi |
| ----------- | ----------- |
| **[postgresql.conf](postgresql.conf.md):**| `Cluster` servisinin başlarken kullandığı ve `Cluster` seviyesinde ayarların |yapıldı dosyadır.
| **[pg_hba.conf](pg_hba.conf.md):**| `Cluster` için, istemci, veritabanı, kullanıcı ve erişim yöntemi gibi birçok erişim |denetimi ayarlarının yapıldığı dosyadır.
| **pg_ident.conf|:** `Cluster` kullanıcı ve sistem kullanıcı eşleştirmesinin yapılması gerekiyorsa buradan yapılmaktadır.|
| **base:**|  Veritabanlarının asıl verisi bulunur.|
| **global:**| `Cluster` genelindeki tablolar burada bulunur. Örn: pg_database|
| **log:**| text logları. erişim logları bulunur.|
| **pg_tblspc:**| Oluşturulan `tablespace`lerin kısa yolları bulunur.|
| **pg_wal:**| `Transaction log`ların tutulduğu dizin. Olabildiğince uzak durulmalıdır. Asla elle silinmemelidir.|


* PostgreSQL'de veritabanları ve tablolar dosya sisteminde dizinlere ve dosyalara (filenode) karşılık gelirler. Bunu görebilmek için


* Bir sonraki:
[servis ve ayar yönetimi](config.md)
