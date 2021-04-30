---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (25. února 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 25. únoru 2020.
author: andreabichsel
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e0ff8fa382ea186426b6f6ceff6044dc35496373
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893369"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (25. února 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.2927. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Povolení entity platformy správy dat (DMF) a navigace správy případů (414754)

Tato ukázková funkce umožňuje další navigaci k případům správy případů. Tuto ukázkovou funkci lze povolit v pracovním prostoru **Správa funkcí**. Tyto položky nabídky se zobrazí v pracovním prostoru **Dodržování předpisů** v aplikaci Dynamics 365 Human Resources. Díky této změně má Human Resources přístup k následujícím prostředkům:

- Všechny případy
- Moje případy
- Moje otevřené případy
- Moje zpožděné případy
- Případy přiřazené mně prostřednictvím workflow

Spolu s těmito novými přehledy případů je k dispozici také entita DMF **Podrobnosti případu**.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Povolení definic vztahů v globálním adresáři (414762)

V globálním adresáři jsou nyní povoleny vztahy. Před vydáním verze tento týden se v okně s fakty **Vztahy** zobrazí všechny systémem definované vztahy. Nyní můžete definovat vztahy v rámci stránky globálního adresáře.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>Lze odebrat pozici, pokud existují aktivní záznamy kompenzace pro danou pozici (414568)

S touto změnou se zobrazí upozornění, pokud se pokusíte odstranit pozici a pracovník má aktivní záznam kompenzace pro stejnou pozici. Pokud k tomu dojde, je nutné před odebráním pozice aktualizovat záznam fixní kompenzace zaměstnance.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>Workflow hodnocení výkonu občas přidává odhlášené osoby, které nejsou součástí procesu (414171)

Tato změna opravuje problém, kdy se do hodnocení výkonu přidávali další odhlášení účastníci.

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>Přiřazení pozice pracovníka není vytvořeno v Dataverse, když je tato možnost vybrána v dialogovém okně Nový pracovník (413479)

Tato změna opravuje problém při zařazení nového pracovníka a jeho přiřazení k pozici prostřednictvím dialogového okna **Nový pracovník**. Nyní se přiřazení pozice projeví v Dataverse.

## <a name="coming-soon"></a>Již brzy

### <a name="updated-dataverse-solution"></a>Aktualizované řešení služby Dataverse

Nové řešení Dataverse bude brzy k dispozici po provedení následujících změn:

| Popis | Změna |
| ----------------------------------------- | --- |
| Změny entity **práce/pozice** | Přidána **Oblast kompenzace**</br>Přidání **finančních dimenzí** |
| Změny entity **pracovníka** | Přidání **sekvence jmen**</br>Přidaná možnost **Práce z domova**</br>Přidán **jazyk**</br>Přidáno **Datum služebního věku**</br>Přidáno **Datum výročí**</br>Přidáno **Datum původního přijetí** |
| Změny **entity zaměstnání** | Přidání **finančních dimenzí**</br>Přidán **Důvod pro výpověď**</br>**Datum ukončení** přejmenováno z **data přechodu**</br>Přidáno **datum zkušební doby** |
| Změny entity **adresy pracovníka** | Přidána **Adresa ulice**</br>**Řádek adresy 1**, **řádek adresy 2** a **řádek adresy 3** označené pro odpis |
| Nové entity nastavení s nastavením variabilní kompenzace | **Typ plánu variabilní kompenzace**</br>**Plán variabilní kompenzace**</br>**Pravidla připsání**</br>**Úroveň plánu variabilní kompenzace** |
| Nová entita **Zaměstnání dle kalendáře pracovníka** | Byla přidána **entita pracovního kalendáře** |
| Nová entita **Mzdové podrobnosti o pozici** | Byla přidána položka **Mzdové podrobnosti o pozici**. |
| Nová entita **Pozice** | Byla přidána položka **Pozice**. Nová entita **Nadpis** bude zahrnuta do procesu synchronizace mezi lidskými zdroji a Dataverse. Na počátku nebude odkazovat z entit **Pracovní pozice** nebo **Úloha**. |

Během příštích několika týdnů budou tyto změny entit k dispozici ve všech prostředích. Postup při ruční instalaci nejnovějšího řešení Dataverse pro Human Resources:

1.  Přejděte do [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com).

2.  Vyberte **Prostředí**.

3.  Vyhledjete prostředí, která chcete upgradovat. To by mělo odpovídat poli **Název prostředí** v sekci **Informace o Common Data Service** ve formuláři **O aplikaci** v modulu Human Resources.

4.  Vyberte prostředí pro zobrazení podrobností o prostředí.

5.  Vyberte možnost **Správa řešení** na panelu akcí nahoře. Otevře se nové okno prohlížeče a přejde do **Centra pro správu Dynamics 365** v kontextu vašeho prostředí.

6.  Na seznamu **Řešení** vyberte možnost **Kotva Dynamics 365 Human Resources**.

7.  Chcete-li použít poslední řešení, vyberte možnost **Upgrade**.

## <a name="in-preview"></a>Náhled

Od 3. února 2020 budou k dispozici následující ukázkové funkce:

- **Funkce náhledu o pracovním volnu a absenci** Další informace získáte v části [Funkce náhledu o pracovním volnu a absenci](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Funkce náhledu správy zaměstnaneckých výhod** - Další informace, včetně známých problémů, získáte v části [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]