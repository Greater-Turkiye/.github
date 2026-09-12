# Yönetişim / Governance

[Türkçe](#türkçe) · [English](#english)

---

## Türkçe

### Roller

| Rol | GitHub ekibi | Yetki | Sorumluluk |
|---|---|---|---|
| Katkıcı | — | Fork + PR | Kurallara uygun katkı |
| Triyajcı | `triagers` | Triage | Issue/PR etiketleme, kopyaları kapatma, eksik bilgi isteme |
| Gözden geçirici | `reviewers` | Write | Veri PR'larını incelemek ve birleştirmek (`CODEOWNERS` kapsamında) |
| Yönetici | `maintainers` | Admin | Organizasyon ayarları, sürümler, yaptırım, erişim, kararlar |

### Terfi yolu

1. **Katkıcı → Triyajcı:** En az 5 birleştirilmiş PR. Kişi kendini veya bir yönetici onu aday gösterir; bir yöneticinin onayı yeterlidir.
2. **Triyajcı → Gözden geçirici:** Yaklaşık 3 ay düzenli katkı, mevcut gözden geçirici veya yöneticilerden **2 kefil** ve **OPSEC bilgilendirmesinin** tamamlanması ([el kitabı — OPSEC](https://github.com/Greater-Turkiye/handbook/blob/main/tr/04-opsec.md)). Yöneticiler onaylar.
3. **Gözden geçirici → Yönetici:** Mevcut yöneticilerin **uzlaşısı** (itiraz eden yönetici olmaması).

Adaylık özel kanaldan yapılır. Takma ad sorun değildir; gerçek kimlik istenmez.

### Karar alma

- Günlük kararlar ilgili depoda PR ve issue üzerinden alınır.
- Organizasyon kararları **yöneticilerin uzlaşısı** ile alınır: öneri yapılır, makul bir süre (en az 72 saat) içinde itiraz gelmezse kabul edilir. İtiraz olursa tartışılır; uzlaşı sağlanamazsa mevcut durum korunur.
- **Temel değişiklikler** (misyon, kırmızı çizgiler, lisans, yönetişim, şemada geriye uyumsuz değişiklik, yayın politikası) [el kitabında bir ADR](https://github.com/Greater-Turkiye/handbook/tree/main/decisions) ile kayda geçirilir. ADR PR'ı en az 7 gün açık kalır. Kırmızı çizgileri gevşeten bir değişiklik tüm yöneticilerin açık onayını gerektirir.

### İnceleme kuralları

- Varsayılan: birleştirme için yazar dışında **en az 1 onay**. Değer `datasets` deposundaki [policy.yaml](https://github.com/Greater-Turkiye/datasets/blob/main/policy.yaml) dosyasında yapılandırılır ve dal koruma kurallarıyla uygulanır.
- Aktif gözden geçirici sayısı **3 veya daha fazla** olduğunda gereken onay sayısı **2'ye** çıkarılır.
- Kimse kendi PR'ını onaylayamaz veya birleştiremez.
- Kırmızı çizgi şüphesi taşıyan bir katkı, bir yönetici görmeden birleştirilmez.
- Otomatik (bot) PR'lar da aynı kurallara tabidir; botlar hiçbir zaman kendi başına birleştiremez.

### Hesap güvenliği

- Organizasyonda **iki aşamalı doğrulama (2FA) zorunludur**; 2FA'sız hesaplar otomatik olarak çıkarılır.
- Güvenlik anahtarı, passkey veya TOTP uygulaması kullanın; SMS kullanmayın.
- Kurtarma kodlarını çevrimdışı saklayın. Parolaları başka yerde yeniden kullanmayın.
- Topluluk için ayrı bir takma adlı hesap önerilir; kişisel hesaplarla ilişkilendirmeyin.
- Gözden geçirici ve yöneticiler cihaz kaybı veya hesap ele geçirilmesi şüphesini derhâl özel kanaldan bildirir.

### Hareketsizlik

- 6 ay boyunca etkinliği olmayan triyajcı, gözden geçirici ve yöneticilere iki hafta önceden haber verilerek yetkileri alınır ve "emeritus" olarak listelenirler.
- Geri dönmek için bir yöneticiye yazmak yeterlidir; yeniden OPSEC bilgilendirmesi istenebilir.
- Organizasyonda her zaman en az **2 aktif yönetici** bulunmalıdır.

### Rolden çıkarma

Davranış kurallarının veya kırmızı çizgilerin ihlali, hesap güvenliğinin ihmali ya da topluluğa zarar veren davranış, [yaptırım basamaklarına](CODE_OF_CONDUCT.md) göre rolün askıya alınmasına veya kaldırılmasına yol açabilir.

---

## English

### Roles

| Role | GitHub team | Permission | Responsibility |
|---|---|---|---|
| Contributor | — | Fork + PR | Contributions that follow the rules |
| Triager | `triagers` | Triage | Label issues/PRs, close duplicates, ask for missing information |
| Reviewer | `reviewers` | Write | Review and merge data PRs (via `CODEOWNERS`) |
| Maintainer | `maintainers` | Admin | Organization settings, releases, enforcement, access, decisions |

### Promotion path

1. **Contributor → Triager:** At least 5 merged PRs. Self-nomination or nomination by a maintainer; one maintainer's approval is enough.
2. **Triager → Reviewer:** About 3 months of regular contribution, **2 vouches** from existing reviewers or maintainers, and a completed **OPSEC briefing** ([handbook — OPSEC](https://github.com/Greater-Turkiye/handbook/blob/main/en/04-opsec.md)). Maintainers approve.
3. **Reviewer → Maintainer:** **Consensus** of the current maintainers (no maintainer objects).

Nominations happen through a private channel. Pseudonyms are fine; no real identity is required.

### Decision making

- Day-to-day decisions are made in PRs and issues of the relevant repository.
- Organization decisions are made by **maintainer consensus**: a proposal is made and, if nobody objects within a reasonable period (at least 72 hours), it is accepted. Objections are discussed; without consensus, the status quo stays.
- **Core changes** (mission, red lines, licence, governance, breaking schema changes, publishing policy) are recorded as an [ADR in the handbook](https://github.com/Greater-Turkiye/handbook/tree/main/decisions). An ADR PR stays open for at least 7 days. Any change that relaxes the red lines requires the explicit approval of every maintainer.

### Review rules

- Default: **at least 1 approval** from someone other than the author before merging. The value is configured in [policy.yaml](https://github.com/Greater-Turkiye/datasets/blob/main/policy.yaml) in the `datasets` repository and enforced by branch protection rules.
- Once there are **3 or more** active reviewers, the required number of approvals is raised to **2**.
- Nobody approves or merges their own PR.
- A contribution suspected of crossing a red line is not merged until a maintainer has seen it.
- Automated (bot) PRs follow the same rules; bots never merge on their own.

### Account security

- **Two-factor authentication (2FA) is mandatory** in the organization; accounts without 2FA are removed automatically.
- Use a security key, passkey or TOTP app; do not use SMS.
- Keep recovery codes offline. Do not reuse passwords elsewhere.
- A separate pseudonymous account for community work is recommended; do not link it to personal accounts.
- Reviewers and maintainers immediately report a lost device or suspected account compromise through the private channel.

### Inactivity

- Triagers, reviewers and maintainers with no activity for 6 months have their permissions removed, with two weeks' notice, and are listed as "emeritus".
- To come back, write to a maintainer; a fresh OPSEC briefing may be required.
- The organization must always have at least **2 active maintainers**.

### Removal from a role

Violations of the code of conduct or the red lines, neglect of account security, or behaviour that harms the community can lead to suspension or removal of a role under the [enforcement ladder](CODE_OF_CONDUCT.md).
