---
title: Přehled správy zaměstnaneckých výhod
description: Přehled funkce správy zaměstnaneckých výhod v Dynamics 365 Human Resources. Nabídněte svým zaměstnancům rozšířené možnosti zaměstnaneckých výhod pomocí snadno použitelného online prostředí.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e2e8fcdd0b6124b459c4dc073e2929418d18bcc5
ms.sourcegitcommit: 084eda1d5503be83e97e2e428e67ef5393535fab
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/17/2020
ms.locfileid: "3819758"
---
# <a name="benefits-management-overview"></a>Přehled správy zaměstnaneckých výhod

Chcete-li si zachovat konkurenceschopnost, musíte nabídnout bohatý soubor zaměstnaneckých výhod, abyste přilákali a udrželi své nejlepší zaměstnance. Kromě standardních výhod, jako je pojištění zdravotní a zubní péče, můžete také nabízet rozšířené služby, např. pomoc s adopcí, rekreační programy a příspěvky na ošacení. Funkce správy zaměstnaneckých výhod ve službě Microsoft Dynamics 365 Human Resources poskytuje flexibilní řešení, které podporuje širokou škálu možností zaměstnaneckých výhod. Aplikace Human Resources také zahrnuje snadno použitelné zaměstnanecké prostředí, které prezentuje vaše nabídky.

- Vylepšené plány zaměstnaneckých výhod vám umožňují vytvářet a spravovat jedinečné plány zaměstnaneckých výhod a podporovat složité tabulky sazeb zaměstnaneckých výhod a vnořené úrovně. Můžete snadno vytvářet programy, balíky a pravidla automatického zařazení pro zaměstnanecké výhody k usnadnění použití zaměstnancem.

- Programy flexibilních kreditů umožňují rozdělit podporu mezi důchod a další životní události.

- Rozsáhlá pravidla způsobilosti zajišťují poskytnutí správných zaměstnaneckých výhod odpovídajícím zaměstnancům.

- Online zařazení do zaměstnaneckých výhod poskytuje vašim zaměstnancům snadno použitelné prostředí.

- Kvalifikované zpracování životních událostí podporuje budoucí žívotní události.

Chcete-li získat přístup k ukázkovým datům, musíte znovu nasadit izolované testovací prostředí (sandbox).

## <a name="enable-benefits-management"></a>Povolení správy zaměstnaneckých výhod

Toto téma popisuje způsob, jakým lze zapnout funkce v aplikaci Human Resources. Také sděluje, které existující funkce v aplikaci Human Resources správa zaměstnaneckých výhod nahradí nebo jsou zakázány po zapnutí správy zaměstnaneckých výhod.

> [!IMPORTANT]
> Po povolení Správy zaměstnaneckých výhod v **Produkčním** prostředí ji již nelze zakázat. Doporučujeme povolit a otestovat Správu zaměstnaneckých výhod v prostředí **Sandbox** před jejím povolením v **Produkčním** prostředí. Existují významné rozdíly mezi staršími funkcemi výhod a novými funkcemi pro správu výhod, které vyžadují další nastavení a měly by být testovány před uvedením do produkce.

- [Správa funkcí](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Konfigurace informací o zaměstnancích

Před zapojením zaměstnanců do zaměstnaneckých výhod je nutné zadat požadované informace. Je nutné, aby byl zaměstnanec zapsán do **Plánu fixní kompenzace** první den a musíte vybrat **Frekvence plateb zaměstnaneckých výhod** v **Podrobnostech o zaměstnání** ve formuláři **Pracovník**.

Pokud máte zaměstnance, který dostává dodatečné odměny, jako jsou provize, můžete přidat částku **Roční výplata benefitů** ze záznamu zaměstnance. Human Resources budou využívat částku **Roční výplata benefitů** při určování částek krytí, namísto pevné roční náhrady. **Roční výplata benefitů** musí platit od počátečního data zaměstnance nebo od začátku období zaměstnaneckých výhod, podle toho, co nastane dříve. Pokud je pro zaměstnance zaznamenána jak pevná odměna, tak roční částka zamšstnaneckých výhod, použije se při stanovení výše krytí roční plat zaměstnaneckých výhod.

Při vytvoření plánu zaměstnaneckých výhod, který používá sazby založené na pohlaví nebo věku, je nutné zadat datum narození a pohlaví zaměstnance pro výpočet nákladů na zaměstnanecké výhody.

## <a name="configure-benefits-management"></a>Konfigurace správy zaměstnaneckých výhod

Před vytvořením plánů zaměstnaneckých výhod pro vaše zaměstnance musíte nakonfigurovat možnosti pro plány.

- [Nastavení parametrů správy zaměstnaneckých výhod](hr-benefits-setup-parameters.md)
- [Konfigurace možností a pravidel způsobilosti](hr-benefits-setup-eligibility-rules.md)
- [Konfigurace možností způsobilosti osobních kontaktů](hr-benefits-setup-contact-eligibility-options.md)
- [Vytvoření možností pokrytí](hr-benefits-setup-coverage-options.md)
- [Nastavení frekvencí platby](hr-benefits-setup-payment-frequencies.md)
- [Konfigurace typů životních událostí](hr-benefits-setup-life-event-types.md)
- [Vytvoření typů plánu](hr-benefits-setup-plan-types.md)
- [Nastavení kódů důvodů](hr-benefits-setup-reason-codes.md)
- [Nastavení kódů úrovně](hr-benefits-setup-tier-codes.md)
- [Konfigurace sazeb](hr-benefits-setup-rates.md)
- [Konfigurace srážek](hr-benefits-setup-deductions.md)
- [Konfigurace dnů čekání](hr-benefits-setup-waiting-days.md)
- [Konfigurace období čekání](hr-benefits-setup-waiting-periods.md)
- [Nastavení pravidel zaokrouhlování](hr-benefits-setup-rounding-rules.md)
- [Vytvoření kategorií zaměstnání](hr-benefits-setup-employment-categories.md)
- [Nastavení typů zaměstnání](hr-benefits-setup-employment-types.md)
- [Konfigurace samoobsluhy pro zaměstnance](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Vytvoření plánů zaměstnaneckých výhod

Tyto články ukazují, jak vytvářet plány zaměstnaneckých výhod, včetně balíků a programů pro pružné kredity.

- [Nastavení plánů zaměstnaneckých výhod](hr-benefits-plans-setup.md)
- [Nastavení programů flexibilních kreditů](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Zpracování plánů zaměstnaneckých výhod

Některé změny je nutné zpracovat, aby byly aktivní.

- [Zpracování způsobilosti k registraci](hr-benefits-process-enrollment-eligibility.md)
- [Zpracování životních událostí](hr-benefits-process-life-events.md)
- [Zpracování změn životních událostí](hr-benefits-process-life-event-changes.md)
- [Zpracování způsobilosti k životním událostem](hr-benefits-process-life-event-eligibility.md)
- [Zpracování změn sazby](hr-benefits-process-rate-changes.md)

