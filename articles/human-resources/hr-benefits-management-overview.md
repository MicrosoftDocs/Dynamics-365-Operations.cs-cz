---
title: Přehled správy zaměstnaneckých výhod
description: Přehled předběžné verze funkce správy zaměstnaneckých výhod v Dynamics 365 Human Resources. Nabídněte svým zaměstnancům rozšířené možnosti zaměstnaneckých výhod pomocí snadno použitelného online prostředí.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029456"
---
# <a name="benefits-management-overview"></a>Přehled správy zaměstnaneckých výhod

[!include [banner](includes/preview-feature.md)]

Chcete-li si zachovat konkurenceschopnost, musíte nabídnout bohatý soubor zaměstnaneckých výhod, abyste přilákali a udrželi své nejlepší zaměstnance. Kromě standardních výhod, jako je pojištění zdravotní a zubní péče, můžete také nabízet rozšířené služby, např. pomoc s adopcí, rekreační programy a příspěvky na ošacení. Předběžná verze funkce správy zaměstnaneckých výhod ve službě Microsoft Dynamics 365 Human Resources poskytuje flexibilní řešení, které podporuje širokou škálu možností zaměstnaneckých výhod. Aplikace Human Resources také zahrnuje snadno použitelné zaměstnanecké prostředí, které prezentuje vaše nabídky.

- Vylepšené plány zaměstnaneckých výhod vám umožňují vytvářet a spravovat jedinečné plány zaměstnaneckých výhod a podporovat složité tabulky sazeb zaměstnaneckých výhod a vnořené úrovně. Můžete snadno vytvářet programy, balíky a pravidla automatického zařazení pro zaměstnanecké výhody k usnadnění použití zaměstnancem.

- Programy flexibilních kreditů umožňují rozdělit podporu mezi důchod a další životní události.

- Rozsáhlá pravidla způsobilosti zajišťují poskytnutí správných zaměstnaneckých výhod odpovídajícím zaměstnancům.

- Online zařazení do zaměstnaneckých výhod poskytuje vašim zaměstnancům snadno použitelné prostředí.

- Kvalifikované zpracování životních událostí je integrováno se samoobslužnými funkcemi pro zaměstnance a také podporuje budoucí životní události.

Chcete-li získat přístup k ukázkovým datům, musíte znovu nasadit izolované testovací prostředí (sandbox).

Můžete poskytnout přímou zpětnou vazbu nebo ohlásit problémy na adresu: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Známé problémy se správou zaměstnaneckých výhod

### <a name="eligibility-processing"></a>Zpracování posouzení nároku

Při spuštění posouzení nároku na zaměstnanecké výhody, které využívají 1–5násobek platu, % platu a paušální částku krytí, musíte nastavit datum **Podrobnosti zaměstnaneckých výhod** na **Počáteční datum zaměstnance** v položce **Historie zaměstnání**. Musíte také zahrnout **Odpracované hodiny**, **Frekvence plateb** a **Roční výše zaměstnaneckých výhod dle platu**. Pokud pracovník dostává pevnou odměnu, zadejte možnost **Odpracované hodiny** a **Frekvence plateb**. Vypočítá se výše ročního platu. Dostává-li zaměstnanec plat, nemusíte zadávat údaj do pole **Odpracované hodiny**. Doporučujeme, abyste při vytváření nových pracovníků nejprve zadali fixní kompenzaci. Chcete-li aktualizovat záznam o podrobnostech zaměstnaneckých výhod, přejděte na stránku **Pracovník > Historie pracovníka > Podrobnosti o zaměstnání**. Upravte datum na počáteční datum pracovníka.

### <a name="employee-self-service"></a>Samoobsluha pro zaměstnance

Částka zaměstnance se při aktualizaci částky krytí pro životní pojištění nepočítá. Pokud je například zaměstnanci nabídnut plán životního pojištění, může vybrat až 50,000 USD v pokrytí při nákladech 0,36 USD na pokrytí 1 000 USD.  Když zaměstnanec aktualizuje částku pokrytí, přiřazené náklady daného zaměstnance budou nulové.

V případě plánu zaměstnaneckých výhod, který umožňuje pouze jeden výběr tohoto typu plánu, obdrží uživatel při pokusu o odpuštění plánu po výběru plánu chybu. Uživatel například vybere lékařský plán a umístí jej do svého nákupního košíku. Uživatel poté vybere **Vzdát se** pro jiný lékařský plán. Uživateli se zobrazí chybová zpráva.

## <a name="enable-benefits-management"></a>Povolení správy zaměstnaneckých výhod

Správa zaměstnaneckých výhod je předběžná verze služby, která je dostupná pouze v **izolovaných testovacích prostředích (sandbox)**. Tyto články popisují způsob, jakým lze zapnout předběžné verze funkcí v aplikaci Human Resources. Také sdělují, které existující funkce v aplikaci Human Resources správa zaměstnaneckých výhod nahradí nebo jsou zakázány po zapnutí správy zaměstnaneckých výhod.

- [Správa funkcí](hr-admin-manage-features.md)
- [Předběžná verze funkce: Správa zaměstnaneckých výhod](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>Konfigurace správy zaměstnaneckých výhod

Před vytvořením plánů zaměstnaneckých výhod pro vaše zaměstnance musíte nakonfigurovat možnosti pro plány.

- [Nastavení parametrů správy zaměstnaneckých výhod](hr-benefits-setup-parameters.md)
- [Konfigurace možností a pravidel způsobilosti](hr-benefits-setup-eligibility-rules.md)
- [Konfigurace možností způsobilosti osobních kontaktů](hr-benefits-setup-contact-eligibility-options.md)
- [Vytvoření možností krytí](hr-benefits-setup-coverage-options.md)
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
- [Vytvoření plánů zaměstnaneckých výhod pracovníka](hr-benefits-plans-worker.md)
- [Nastavení programů flexibilních kreditů](hr-benefits-plans-flex-credit-programs.md)
- [Konfigurace budoucích životních událostí](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Zpracování plánů zaměstnaneckých výhod

Některé změny je nutné zpracovat, aby byly aktivní.

- [Zpracování způsobilosti k registraci](hr-benefits-process-enrollment-eligibility.md)
- [Zpracování životních událostí](hr-benefits-process-life-events.md)
- [Zpracování změn životních událostí](hr-benefits-process-life-event-changes.md)
- [Zpracování způsobilosti k životním událostem](hr-benefits-process-life-event-eligibility.md)
- [Zpracování změn sazby](hr-benefits-process-rate-changes.md)

