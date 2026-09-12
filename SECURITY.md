# Güvenlik ve Hassas İçerik Politikası / Security & Sensitive Content Policy

[Türkçe](#türkçe) · [English](#english)

<!-- <ORG_EMAIL>: kurumsal e-posta kutusu henüz yok; oluşturulduğunda bu dosyadaki tüm <ORG_EMAIL> yer tutucuları gerçek adresle değiştirilecek.
     <ORG_EMAIL>: there is no org mailbox yet; every <ORG_EMAIL> placeholder in this file will be replaced with the real address once it exists. -->

---

## Türkçe

### Neyi bildirmelisiniz?

1. **Güvenlik açıkları** — araçlarda (`tools/gt.py`), platform kodunda, GitHub Actions iş akışlarında, açığa çıkmış anahtar veya token'lar.
2. **Hassas içerik** — depolarda, commit geçmişinde veya yayın kanallarımızda gördüğünüz:
   - kişisel veri (özel kişilerin adı, yüzü, adresi, telefonu, hesabı vb.),
   - gizli veya sızdırılmış materyal,
   - yanlışlıkla paylaşılmış Türk kuvvetlerine ait konum veya hareket bilgisi,
   - esir veya kayıp görüntüsü.
3. **Kaldırma talepleri** — telif hakkı, kişisel veri veya başka bir hukuki gerekçeyle içeriğin kaldırılması isteği.

### Nasıl bildirilir?

**Asla herkese açık issue, PR, Tartışma veya yorum kullanmayın.** İçeriği alıntılamayın, yeniden paylaşmayın; yalnızca konumunu (bağlantı, kayıt kimliği, commit SHA'sı) belirtin.

Özel kanallar:

1. **GitHub özel güvenlik bildirimi (şimdi kullanılabilir):** İlgili deponun **Security** sekmesinde **"Report a vulnerability"** düğmesi. Örneğin:
   - veri içeriği için: <https://github.com/Greater-Turkiye/datasets/security/advisories/new>
   - genel veya hangi depo olduğundan emin değilseniz: <https://github.com/Greater-Turkiye/.github/security/advisories/new>
2. **E-posta:** `<ORG_EMAIL>` (henüz etkin değil; yukarıdaki nota bakın).

Bildiriminize ekleyin: içeriğin konumu, sorunun kısa açıklaması, varsa talebinizin hukuki gerekçesi ve (isteğe bağlı) size nasıl dönüş yapılacağı.

### Yanıt hedefleri

Gönüllü bir topluluğuz; aşağıdakiler en iyi çaba hedefleridir.

| Tür | İlk yanıt | İşlem |
|---|---|---|
| Hassas içerik / kaldırma talebi | 72 saat içinde | 72 saat içinde kaldırma veya gizleme |
| Açığa çıkmış anahtar/token | Mümkün olan en kısa sürede | Anahtar derhâl iptal edilir |
| Diğer güvenlik açıkları | 7 gün içinde | Önem derecesine göre planlanır |

### Sonra ne olur?

1. Bildirim iki yönetici tarafından değerlendirilir.
2. Uygunsa kayıt silinir ve yerine bir **tombstone** (mezar taşı) kaydı konur: kimlik korunur, içerik kaldırılır, yalnızca kaldırma nedeni kategorisi kalır.
3. İçerik commit geçmişinde zarar vermeye devam ediyorsa geçmiş yeniden yazılır ve önbelleğe alınmış görünümlerin ve PR referanslarının temizlenmesi için **GitHub Destek'ten silme talebinde** bulunulur.
4. İçerik yayın kanallarımızda paylaşıldıysa gönderi silinir ve gerekiyorsa bir düzeltme gönderisi yayımlanır.
5. İşlem özel bir kayıt defterine işlenir; bildirimde bulunana sonuç bildirilir.

Not: Fork'lar ve üçüncü taraf kopyalar üzerinde doğrudan denetimimiz yoktur; gerekirse GitHub'ın kendi kaldırma süreçlerine başvururuz.

### Kapsam ve iyi niyet

Yalnızca `main` dalı ve aktif olarak işletilen hizmetler desteklenir. İyi niyetle yapılan güvenlik araştırmasını memnuniyetle karşılarız; başkalarının hesaplarına veya verilerine erişmeye çalışmayın, hizmet dışı bırakma testi yapmayın ve sorun düzeltilmeden ayrıntıları kamuya açıklamayın.

---

## English

### What to report

1. **Security vulnerabilities** — in tools (`tools/gt.py`), platform code, GitHub Actions workflows, or exposed keys and tokens.
2. **Sensitive content** — anything you see in our repositories, commit history or publishing channels that contains:
   - personal data (names, faces, addresses, phone numbers, accounts, etc. of private individuals),
   - classified or leaked material,
   - position or movement information on Turkish forces posted by mistake,
   - imagery of prisoners of war or casualties.
3. **Takedown requests** — requests to remove content on copyright, personal data or other legal grounds.

### How to report

**Never use a public issue, PR, Discussion or comment.** Do not quote or repost the content; only point to where it is (link, record ID, commit SHA).

Private channels:

1. **GitHub private vulnerability reporting (available now):** the **"Report a vulnerability"** button under the **Security** tab of the relevant repository. For example:
   - for data content: <https://github.com/Greater-Turkiye/datasets/security/advisories/new>
   - general, or if you are unsure which repository: <https://github.com/Greater-Turkiye/.github/security/advisories/new>
2. **Email:** `<ORG_EMAIL>` (not active yet; see the note above).

Please include: where the content is, a short description of the problem, the legal basis of your request if any, and (optionally) how we can reach you.

### Response targets

We are a volunteer community; these are best-effort targets.

| Type | First response | Action |
|---|---|---|
| Sensitive content / takedown request | Within 72 hours | Removed or hidden within 72 hours |
| Exposed key/token | As soon as possible | Key revoked immediately |
| Other vulnerabilities | Within 7 days | Scheduled according to severity |

### What happens next

1. Two maintainers assess the report.
2. If justified, the record is deleted and replaced by a **tombstone** record: the ID is kept, the content is removed, and only the removal reason category remains.
3. If the content remains harmful in commit history, history is rewritten and a removal request is sent to **GitHub Support** to purge cached views and PR references.
4. If the content was posted on our publishing channels, the post is deleted and, where needed, a correction post is published.
5. The action is logged in a private register and the reporter is informed of the outcome.

Note: we have no direct control over forks and third-party copies; where necessary we use GitHub's own removal processes.

### Scope and good faith

Only the `main` branch and actively operated services are supported. We welcome good-faith security research; do not try to access other people's accounts or data, do not run denial-of-service tests, and do not disclose details publicly before the issue is fixed.
