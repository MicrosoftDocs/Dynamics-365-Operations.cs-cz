---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (10. března 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 10. březnu 2020.
author: Darinkramer
manager: AnnBe
ms.date: 03/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 944481727f3222a10f128ac3078c117f5ae7d193
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526901"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (10. března 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.2985. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Nelze získat přístup k sestavě analýzy dovednostních mezer (394460)

Tato sestava není podporována v aplikaci Dynamics 365 Human Resources. Položka nabídky pro tisk sestavy SSRS je odebrána.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Nesprávná zpráva při přístupu na stránku Začínáme (417950)

Při této změně zabezpečení skryje tuto položku nabídky v případě, že nemáte přístup k formuláři.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Zjednodušená údržba úkolů pro zaměstnance (380538)

Ve formuláři údržby úkolů pracovníka jsou uvedeny všechny úkoly pro zaměstnance v rámci náboru, odchodu, přechodu a obchodních procesů. Stav úkolů můžete buď odstranit, znovu přiřadit nebo aktualizovat.

Příklad: Benjamin Martin je správcem zaměstnaneckých výhod. Během náboru zaměstnanců jsou úkoly vytvářeny pro Benjamina, aby zkontroloval výběr výhod zaměstnanců. Benjamin má dřívější úkoly, které byly dokončeny, a budoucí úkoly, které musí být dokončeny. Benjamin se rozhodne opustit společnost, takže jeho úkoly musí být znovu přiřazeny nebo odstraněny. Formulář správy úkolů (v podokně akcí ve formuláři **Pracovník**) umožňuje, aby byly všechny Benjaminovy úkoly znovu přiřazeny jinému pracovníkovi nebo odstraněny.  

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Řešení Common Data Service je nyní k dispozici s následujícími změnami:

| popis | Vrácená hotovost |
| --- | --- |
| Změny entity **práce/pozice** | <ul><li>Přidána **Oblast kompenzace**</li>|
| Byla přidána entita **Dimenze pracovní pozice** | <ul><li>Přidání **finančních dimenzí**</li>
| Změny entity **pracovníka** | <ul><li>Přidání **sekvence jmen**</li><li>Přidaná možnost **Práce z domova**</li><li>Přidán **jazyk**</li><li>Přidáno **Datum služebního věku**</li><li>Přidáno **Datum výročí**</li><li>Přidáno **Datum původního přijetí**</li></ul> |
| Změny **entity zaměstnání** | <ul><li>Přidání **finančních dimenzí**</li><li>Přidán **Důvod pro výpověď**</li><li>**Datum ukončení** přejmenováno z **data přechodu**</li><li>Přidáno **datum zkušební doby**</li></ul> |
| Změny entity **adresy pracovníka** | <ul><li>Přidána **Adresa ulice**</li><li>**Řádek adresy 1**, **řádek adresy 2** a **řádek adresy 3** označené pro odpis</li></ul> |
| Nové entity nastavení s nastavením variabilní kompenzace | <ul><li>**Typ plánu variabilní kompenzace**</li><li>**Plán variabilní kompenzace**</li><li>**Pravidla připsání**</li><li>**Úroveň plánu variabilní kompenzace**</li></ul> |
| Nová entita **Zaměstnání dle kalendáře pracovníka** | <ul><li>Byla přidána **entita pracovního kalendáře**</li></ul> |
| Nová entita **Mzdové podrobnosti o pozici** | <ul><li>Byla přidána položka **Mzdové podrobnosti o pozici**.</li></ul> |
| Nová entita **Pozice** | <ul><li>Přidána položka **Pozice**</li></ul> Nová entity **Pozice** je zahrnuta do Common Data Service, ale tentokrát neodkazuje z entit **Pracovní pozice** nebo **Práce**. |

> [!NOTE]
> Finanční dimenze pro pracovní pozice i zaměstnanost poskytují integraci jedním směrem pro aktualizace z modulu Human Resources do Common Data Service. Aktualizace finančních dimenzí nejsou v současné době synchronizovány z Common Data Service do modulu Human Resources.

Během příštích několika týdnů budou tyto změny entit k dispozici ve všech prostředích. Postup při ruční instalaci nejnovějšího řešení Common Data Service pro Human Resources:

1.  Přejděte do [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com).

2.  Vyberte **Prostředí**.

3.  Vyhledjete prostředí, která chcete upgradovat. Prostředí by mělo odpovídat poli **Název prostředí** v sekci **Informace o Common Data Service** ve formuláři **O aplikaci** v modulu Human Resources.

4.  Vyberte prostředí pro zobrazení podrobností o prostředí.

5.  Vyberte možnost **Správa řešení** na panelu akcí nahoře. Otevře se nové okno prohlížeče a přejde do **Centra pro správu Dynamics 365** v kontextu vašeho prostředí.

6.  Na seznamu **Řešení** vyberte možnost **Kotva Dynamics 365 Human Resources**.

7.  Chcete-li použít poslední řešení, vyberte možnost **Upgrade**.

## <a name="in-preview"></a>Náhled

Od 3. února 2020 jsou k dispozici následující funkce náhledu:

- **Funkce náhledu o pracovním volnu a absenci** Další informace získáte v části [Funkce náhledu o pracovním volnu a absenci](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Funkce náhledu správy zaměstnaneckých výhod** - Další informace, včetně známých problémů, získáte v části [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Již brzy

### <a name="platform-update-33"></a>Platform update 33

- Aplikace přes celou stránku (Preview) – Tato ukázková funkce, která vyžaduje povolení funkce Uložená zobrazení, umožňuje přidání aplikací Power Apps a aplikací třetích stran v zobrazení přes celou stránku prostřednictvím řídicího panelu.

- Uložená zobrazení (Preview) – Tato ukázková funkce povoluje uložená zobrazení, což je významné rozšíření podsystému individuálního nastavení. Tato funkce umožňuje uživatelům vlastnit více pojmenovaných sad individuálních nastavení na stránku. Zobrazení lze také publikovat v rolích zabezpečení.

- Optimalizovaná funkce filtrování „je jedna z“ – Tato funkce umožňuje optimalizaci funkce filtrování „je jedna z“, které usnadňuje zadání více hodnot filtru, má jednodušší mechanismus k odebrání jednotlivých nebo všech hodnot filtru a má kompaktnější a intuitivnější vizualizace hodnot filtru.

- Doporučená pole – Uživatelé často potřebují přidávat pole do mřížky nebo na stránku. To může být obtížné s tolika dostupnými poli. Tato funkce místo prohledávání rozsáhlého seznamu umožňuje systému vytáhnout sadu doporučených polí podle toho, co jiní uživatelé nejčastěji přidávají v podobných situacích.

- Výchozí akce jedním prstem v mřížkách – Touto funkcí je zajištěno, že výchozí akce v mřížce je propojena s určitým sloupcem v mřížce bez ohledu na to, zda je tento sloupec přesunut nebo skryt.

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]