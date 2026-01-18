🚀 Antigravity Skills

Bu depo, Antigravity programı için geliştirilmiş, yeniden kullanılabilir ve standartlaştırılmış skills (yetenek tanımları) içerir.

Bu skills’lerin amacı; yapay zekâ destekli proje üretim ve inceleme süreçlerinde tutarlılığı, doğruluğu ve birebir uyumu garanti altına almaktır.

Bu repo bir dokümantasyon arşivi değil; Antigravity’nin nasıl davranması gerektiğini tanımlayan davranış sözleşmeleridir.

⸻

📦 Repo İçeriği

antigravity-skills/
├─ skills/
│  ├─ code-review.md
│  └─ project-parity-guard.md
├─ README.md
└─ LICENSE


⸻

🧠 Skills Nedir?

Skill, Antigravity programına:
	•	hangi durumda ne yapacağını,
	•	nasıl düşüneceğini,
	•	hangi kurallara uymak zorunda olduğunu

öğreten, Markdown tabanlı bir davranış tanımıdır.

Bu repo’daki skills:
	•	prompt değildir
	•	örnek kod değildir
	•	kuralsız rehber değildir

Her biri kesin kurallar, adımlar ve çıktı formatları tanımlar.

⸻

🧩 Mevcut Skills

1️⃣ Code Review Skill

Dosya: skills/code-review.md

Bu skill, Antigravity’nin bir projedeki kod değişikliklerini standart, tutarlı ve profesyonel şekilde incelemesini sağlar.

🎯 Amaç
	•	Kodun sadece çalışmasını değil, sürdürülebilir olmasını sağlamak
	•	İnceleme sürecinde kişisel değil, kod odaklı geri bildirim üretmek
	•	Junior → Senior reviewer davranışlarını netleştirmek

🔍 İncelediği Alanlar
	•	Doğruluk (Correctness)
	•	Mimari & Temiz Kod
	•	Performans & Ölçeklenebilirlik
	•	Güvenlik & Sağlamlık
	•	Test & Dokümantasyon

👥 Reviewer Seviyeleri
	•	Junior Reviewer → Okunabilirlik ve temel hatalar
	•	Mid-Level Reviewer → Performans, SOLID, edge-case
	•	Senior Reviewer (Antigravity Standard) → Mimari etki, teknik borç, yönlendirme

🏷️ Yorum Etiketleri
	•	[BLOCKER] – Düzeltilmeden merge edilemez
	•	[SUGGESTION] – Güçlü öneri
	•	[NITPICK] – Küçük, engelleyici olmayan detay
	•	[QUESTION] – Anlamak için soru
	•	[KUDOS] – Takdir ve pozitif geri bildirim

Bu skill, PR review, kod denetimi ve AI destekli code audit senaryolarında kullanılır.

⸻

2️⃣ Project Parity Guard

Dosya: skills/project-parity-guard.md

Bu skill, Antigravity’ye verilen hazır referans kodlar ile, bu kodlardan üretilen projenin birebir aynı olmasını garanti altına alır.

Amaç: “Ben sana birebir aynı projeyi istedim” beklentisini teknik olarak zorunlu kılmak.

🎯 Amaç
	•	Referans kod = tek doğru kaynak (source of truth)
	•	Üretilen proje ile referans arasında:
	•	dosya yapısı
	•	dosya isimleri
	•	içerik (byte-for-byte)

birebir uyum sağlamak

🔍 Yaptığı Kontroller
	•	Dosya ağacı karşılaştırması
	•	Eksik / fazla dosya tespiti
	•	İçerik hash (SHA-256) karşılaştırması
	•	Whitespace / newline / encoding farkları
	•	Taşınmış veya yeniden adlandırılmış dosyalar

🛠️ Davranışı
	•	Referansı asla iyileştirmez
	•	Sadece eksik veya hatalı kısımları minimal patch ile düzeltir
	•	Gerekirse dosyayı komple birebir kopyalar
	•	Sonunda tekrar doğrulama yapar

📊 Çıktı
Skill, her çalışmada şunları üretir:
	•	Parity durumu (PASS / FAIL)
	•	Bulunan farkların listesi
	•	Yapılan düzeltmeler
	•	Nihai doğrulama sonucu

Bu skill özellikle:
	•	AI ile proje scaffold oluşturma
	•	Template → proje üretimi
	•	Kurumsal “aynısı olsun” beklentileri

için kritiktir.

⸻

⚙️ Kullanım

İstediğin skill dosyasını Antigravity projenin ilgili klasörüne kopyalaman yeterlidir:

/skills

Antigravity, skill’i dosyanın YAML front matter kısmından tanır:

name:
description:

Başka bir konfigürasyon gerekmez.

⸻

📜 Lisans

Bu repo MIT Lisansı ile paylaşılmaktadır.
	•	Ticari kullanıma açıktır
	•	Değiştirilebilir
	•	Dağıtılabilir

⸻

🧭 Son Not

Bu skills’ler:
	•	“daha iyi prompt” yazmak için değil,
	•	daha doğru davranan sistemler kurmak için vardır.

Antigravity büyüdükçe bu repo da büyüyecek.

Standartlar yaşayan şeylerdir.
