# Katkı Rehberi / Contributing Guide

[Türkçe](#türkçe) · [English](#english)

Depoya özel rehberler bu dosyadan önceliklidir / Repository-specific guides take precedence over this file:

- Veri / Data: [datasets/CONTRIBUTING.md](https://github.com/Greater-Turkiye/datasets/blob/main/CONTRIBUTING.md)
- El kitabı / Handbook: [tr/10-contributing.md](https://github.com/Greater-Turkiye/handbook/blob/main/tr/10-contributing.md) · [en/10-contributing.md](https://github.com/Greater-Turkiye/handbook/blob/main/en/10-contributing.md)

---

## Türkçe

Katkıda bulunmadan önce [Kırmızı çizgiler](https://github.com/Greater-Turkiye/handbook/blob/main/tr/02-red-lines.md) ve OPSEC sayfalarını okuyun. Bu sayfalar isteğe bağlı değildir.

### Katkı yolları

| Ne? | Nerede? | Nasıl? |
|---|---|---|
| Olay önerisi | `datasets` | "Veri önerisi" issue formu veya doğrudan kayıt PR'ı (`python tools/gt.py new event`) |
| Kaynak önerisi | `datasets` | "Kaynak önerisi" issue formu |
| Düzeltme | `datasets` | "Düzeltme" issue formu veya PR |
| Sözlük önerisi | `datasets` | "Sözlük önerisi" issue formu |
| El kitabı çevirisi ve düzeltmeleri | `handbook` | `tr/` ve `en/` sayfalarının eşzamanlı tutulması |
| Kod | `platform` | [ROADMAP](https://github.com/Greater-Turkiye/platform/blob/main/ROADMAP.md) içindeki işler |
| İnceleme | tüm depolar | Açık PR'ları okuyup kaynakları kontrol etmek; onay yetkisi olmadan da yorum yapılabilir |

### Fork ve PR akışı

Organizasyon dışındaki herkes fork üzerinden çalışır.

1. Depoyu fork'layın ve klonlayın.
2. Anlamlı adla bir dal açın: `data/evt-ege-tatbikat`, `docs/opsec-typo`, `feat/rss-collector`.
3. Değişikliği yapın. Veri deposunda `python tools/gt.py validate` komutunun hatasız geçtiğinden emin olun.
4. Commit'leyin (aşağıdaki kurallara bakın) ve fork'unuza gönderin.
5. PR açın ve PR şablonundaki kontrol listesini eksiksiz doldurun.
6. İnceleme yorumlarına yanıt verin. Onay ve başarılı CI sonrası bir gözden geçirici birleştirir (squash merge).

Küçük PR'lar tercih edilir: bir PR = bir kayıt veya bir konu.

### Commit hijyeni

Commit meta verileri herkese açıktır ve silinmesi zordur.

- **E-posta:** GitHub'ın `noreply` adresini kullanın. GitHub → Settings → Emails bölümünde "Keep my email addresses private" ve "Block command line pushes that expose my email" seçeneklerini açın.

  ```sh
  git config user.email "<ID>+<kullanici-adi>@users.noreply.github.com"
  ```

- **Saat dilimi:** Commit zaman damgaları yerel saat diliminizi gösterir. UTC kullanın:

  ```sh
  # bash / zsh
  export TZ=UTC
  # PowerShell
  $env:TZ = "UTC"
  ```

- **Dosyalar:** Görsel eklemeden önce EXIF/konum meta verilerini silin. Tarayıcı geçmişi, ekran görüntüsündeki kişisel sekme/bildirimler gibi izleri kontrol edin.
- **Mesajlar:** Kısa, emir kipinde, önekli: `data: evt_... ekle`, `fix: ...`, `docs: ...`, `vocab: ...`, `feat: ...`.
- **Asla** parola, token, API anahtarı veya `.env` dosyası commit'lemeyin. Yanlışlıkla gönderdiyseniz hemen [SECURITY.md](SECURITY.md) üzerinden bildirin ve anahtarı iptal edin.

### PR beklentileri

- Şablondaki tüm kutular işaretli ya da işaretlenmeme nedeni yazılı olmalıdır.
- Her iddianın kaynağı ve mümkünse arşiv bağlantısı bulunmalıdır.
- CI geçmelidir; varsayılan olarak yazar dışında en az bir onay gerekir ([GOVERNANCE.md](GOVERNANCE.md)).
- İnceleme başladıktan sonra zorla gönderme (force-push) yerine yeni commit ekleyin.
- 30 gün yanıtsız kalan PR'lar kapatılabilir; istediğiniz zaman yeniden açabilirsiniz.

### Etiketler

| Etiket | Anlamı |
|---|---|
| `triage` | Henüz değerlendirilmedi |
| `data-submission` | Olay/kayıt önerisi |
| `source-suggestion` | Yeni kaynak önerisi |
| `correction` | Mevcut kayıtta hata |
| `vocab-proposal` | Sözlük değişikliği önerisi |
| `bug` | Araç veya platformda hata |
| `enhancement` | Yeni özellik veya iyileştirme |
| `docs` | Belgelendirme |
| `good first issue` | Yeni başlayanlara uygun |
| `help wanted` | Yardım aranıyor |

### Nereye sorarım?

Sorular ve fikirler için [Tartışmalar](https://github.com/orgs/Greater-Turkiye/discussions). Ayrıntı: [SUPPORT.md](SUPPORT.md). Hassas konular için [SECURITY.md](SECURITY.md).

### Lisans

Bir PR açarak katkınızı ilgili deponun lisansı altında sunmayı kabul etmiş olursunuz (inbound = outbound): içerik ve veriler **CC BY 4.0**, kod **MIT**. Ayrı bir CLA veya DCO imzası gerekmez. Başkasına ait metni kopyalamayın; özetleyin ve kaynağı gösterin.

---

## English

Before contributing, read the [Red lines](https://github.com/Greater-Turkiye/handbook/blob/main/en/02-red-lines.md) and OPSEC pages. They are not optional.

### Ways to contribute

| What | Where | How |
|---|---|---|
| Event submission | `datasets` | "Data submission" issue form, or a record PR directly (`python tools/gt.py new event`) |
| Source suggestion | `datasets` | "Source suggestion" issue form |
| Correction | `datasets` | "Correction" issue form or a PR |
| Vocabulary proposal | `datasets` | "Vocabulary proposal" issue form |
| Handbook translation and fixes | `handbook` | Keep `tr/` and `en/` pages in sync |
| Code | `platform` | Tasks in the [ROADMAP](https://github.com/Greater-Turkiye/platform/blob/main/ROADMAP.md) |
| Review | all repositories | Read open PRs and check the sources; anyone can comment even without approval rights |

### Fork-and-PR flow

Everyone outside the organization teams works from a fork.

1. Fork and clone the repository.
2. Create a descriptive branch: `data/evt-aegean-exercise`, `docs/opsec-typo`, `feat/rss-collector`.
3. Make the change. In the datasets repository, make sure `python tools/gt.py validate` passes without errors.
4. Commit (see the rules below) and push to your fork.
5. Open a PR and complete the checklist in the PR template.
6. Respond to review comments. After approval and green CI, a reviewer merges (squash merge).

Small PRs are preferred: one PR = one record or one topic.

### Commit hygiene

Commit metadata is public and hard to remove.

- **Email:** Use your GitHub `noreply` address. In GitHub → Settings → Emails, enable "Keep my email addresses private" and "Block command line pushes that expose my email".

  ```sh
  git config user.email "<ID>+<username>@users.noreply.github.com"
  ```

- **Time zone:** Commit timestamps reveal your local time zone. Use UTC:

  ```sh
  # bash / zsh
  export TZ=UTC
  # PowerShell
  $env:TZ = "UTC"
  ```

- **Files:** Strip EXIF/location metadata from images before adding them. Check screenshots for personal tabs, notifications or other traces.
- **Messages:** Short, imperative, prefixed: `data: add evt_...`, `fix: ...`, `docs: ...`, `vocab: ...`, `feat: ...`.
- **Never** commit passwords, tokens, API keys or `.env` files. If you pushed one by mistake, report it immediately via [SECURITY.md](SECURITY.md) and revoke the key.

### PR expectations

- Every box in the template is ticked, or the reason for not ticking it is written down.
- Every claim has a source and, where possible, an archive link.
- CI must pass; by default at least one approval from someone other than the author is required ([GOVERNANCE.md](GOVERNANCE.md)).
- After review has started, add new commits instead of force-pushing.
- PRs without a response for 30 days may be closed; you can reopen them any time.

### Labels

| Label | Meaning |
|---|---|
| `triage` | Not yet assessed |
| `data-submission` | Event/record submission |
| `source-suggestion` | New source suggestion |
| `correction` | Error in an existing record |
| `vocab-proposal` | Vocabulary change proposal |
| `bug` | Bug in tools or platform |
| `enhancement` | New feature or improvement |
| `docs` | Documentation |
| `good first issue` | Suitable for newcomers |
| `help wanted` | Help wanted |

### Where to ask

Questions and ideas go to [Discussions](https://github.com/orgs/Greater-Turkiye/discussions). Details: [SUPPORT.md](SUPPORT.md). Sensitive matters: [SECURITY.md](SECURITY.md).

### Licence

By opening a PR you agree to license your contribution under the licence of that repository (inbound = outbound): content and data **CC BY 4.0**, code **MIT**. No separate CLA or DCO sign-off is required. Do not copy other people's text; summarize it and cite the source.
