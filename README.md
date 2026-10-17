# Greater-Turkiye/.github

[Türkçe](#türkçe) · [English](#english)

## Türkçe

Bu depo, Greater Türkiye organizasyonunun **profil sayfasını** ve **varsayılan topluluk sağlığı dosyalarını** barındırır. Organizasyondaki bir depo bu dosyaların kendi sürümünü içermiyorsa GitHub buradakileri otomatik olarak kullanır.

| Dosya / klasör | Amaç |
|---|---|
| `profile/README.md` | github.com/Greater-Turkiye adresindeki açılış sayfası |
| `CODE_OF_CONDUCT.md` | Davranış kuralları, kırmızı çizgiler eki ve yaptırım basamakları |
| `CONTRIBUTING.md` | Organizasyon genelinde katkı rehberi |
| `GOVERNANCE.md` | Roller, terfi yolu, karar alma, inceleme kuralları |
| `SECURITY.md` | Güvenlik açıkları, hassas içerik ve kaldırma talepleri için özel kanal |
| `SUPPORT.md` | Hangi soru nereye sorulur |
| `ISSUE_TEMPLATE/` | Varsayılan issue formları |
| `PULL_REQUEST_TEMPLATE.md` | Varsayılan PR kontrol listesi |
| `DISCUSSION_TEMPLATE/` | Tartışma kategori formları |
| `LICENSE` | Bu depodaki dosyalar için MIT lisansı |

Notlar:

- Bir depo kendi `.github/ISSUE_TEMPLATE/` klasörünü içeriyorsa buradaki issue formları o depoda **hiç kullanılmaz**; GitHub klasörü dosya dosya birleştirmez.
- Kaldırma talepleri ve hassas içerik bildirimleri için issue formu **yoktur**; bunlar yalnızca [SECURITY.md](SECURITY.md) içinde tarif edilen özel kanaldan iletilir.
- Buradaki bir dosyayı değiştirmek organizasyondaki tüm depoları etkiler; bu nedenle değişiklikler bir yöneticinin onayını gerektirir.

## Issue'ları Claude çözer

`.github/workflows/claude-issues.yml`, organizasyondaki her deponun kendi `.github/workflows/claude.yml` dosyasından çağrılır ve GitHub Actions içinde çalışır; kimsenin bilgisayarının açık olması gerekmez.

- Yeni bir issue açıldığında `vars.GT_ISSUE_OWNER` kişisine (varsayılan `choi303`) atanır, bildirim hemen gider.
- Claude Code (`vars.CLAUDE_MODEL`, varsayılan `claude-opus-5-5`; `vars.CLAUDE_EFFORT`, varsayılan `medium`) issue'yu baştan sona çözer: dal, değişiklik, CI, PR, squash-merge ve issue'ya kısa bir özet.
- Yeni issue, `claude` etiketi ya da `@claude` geçen bir yorum tetikler. Veri, kaynak, düzeltme, sözlük, üyelik ve bilgi talebi formları kendi akışlarıyla kalır; `claude` etiketi eklenmedikçe atlanır.
- Yalnızca depoya yazma yetkisi olan kişiler tetikleyebilir.
- Dal kuralı onay istiyorsa Claude kuralı aşmaz: incelemeyi sahibinden ister, otomatik birleştirmeyi açar; onay gelince PR kendiliğinden birleşir.
- Gerekenler: `secrets.CLAUDE_CODE_OAUTH_TOKEN` (`claude setup-token`) ve organizasyon ayarlarında "Allow GitHub Actions to create and approve pull requests". İsteğe bağlı `secrets.GT_BOT_TOKEN`, PR kontrollerinin kendiliğinden başlamasını sağlar. `vars.CLAUDE_ISSUES=off` her yerde durdurur.

## English

This repository holds the Greater Türkiye organisation's **profile page** and **default community health files**. GitHub falls back to these files for any repository in the organisation that does not have its own version.

| File / folder | Purpose |
|---|---|
| `profile/README.md` | Landing page at github.com/Greater-Turkiye |
| `CODE_OF_CONDUCT.md` | Code of conduct, with the red lines annex and enforcement ladder |
| `CONTRIBUTING.md` | Contribution guide for the whole organisation |
| `GOVERNANCE.md` | Roles, promotion path, decision-making and review rules |
| `SECURITY.md` | Private channel for reporting vulnerabilities, sensitive content and takedown requests |
| `SUPPORT.md` | Where to ask which question |
| `ISSUE_TEMPLATE/` | Default issue forms |
| `PULL_REQUEST_TEMPLATE.md` | Default PR checklist |
| `DISCUSSION_TEMPLATE/` | Discussion category forms |
| `LICENSE` | MIT licence covering the files in this repository |

Notes:

- If a repository has its own `.github/ISSUE_TEMPLATE/` folder, **none** of the issue forms here are used in that repository; GitHub does not merge the two folders file by file.
- There is **no** issue form for takedown requests or reports of sensitive content; these go only through the private channel described in [SECURITY.md](SECURITY.md).
- Changes here affect every repository in the organisation, so they require a maintainer's approval.

## Issues are worked by Claude

`.github/workflows/claude-issues.yml` is called from each repository's own `.github/workflows/claude.yml` and runs in GitHub Actions, so nobody's computer needs to be on.

- A new issue is assigned to `vars.GT_ISSUE_OWNER` (default `choi303`), who is notified at once.
- Claude Code (`vars.CLAUDE_MODEL`, default `claude-opus-5-5`; `vars.CLAUDE_EFFORT`, default `medium`) resolves it end to end: branch, change, CI, pull request, squash-merge and a short summary on the issue.
- A new issue, the `claude` label or a comment containing `@claude` starts it. Data, source, correction, vocabulary, membership and RFI forms keep their own flows and are skipped unless the `claude` label is added.
- Only people with write access to the repository can start it.
- Where the branch rules require an approving review, Claude never bypasses them: it requests the review from the owner and turns on auto-merge, so the pull request merges once approved.
- Needs `secrets.CLAUDE_CODE_OAUTH_TOKEN` (`claude setup-token`) and the organisation setting "Allow GitHub Actions to create and approve pull requests". The optional `secrets.GT_BOT_TOKEN` makes the pull request checks start on their own. `vars.CLAUDE_ISSUES=off` stops it everywhere.

## Depo kurallari / Repository rules

Yapay zeka araclari ve yeni katkicilar icin kisa calisma kurallari: [CLAUDE.md](CLAUDE.md). Bu kurallarin ilki, her degisiklikte README dosyasini ayni PR icinde guncel tutmaktir.
Short working rules for AI agents and new contributors: [CLAUDE.md](CLAUDE.md). The first of them is keeping the README true in the same pull request as the change.
