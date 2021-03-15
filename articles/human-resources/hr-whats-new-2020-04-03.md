---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (3. dubna 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 3. dubnu 2020.
author: andreabichsel
manager: tfehr
ms.date: 04/03/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b00ef61cdd7ceac6c6f57187a0e6c98e94c8cb71
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127914"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (3. dubna 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3111. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory pro referenci v Lifecycle Services (LCS).

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>Funkce, které jsou dispozici v týdnu od 6. dubna

- **Funkce pracovního volna a absence** - více informací naleznete v [Přehledu pracovního volna a absence](hr-leave-and-absence-overview.md).

- **Funkce správy zaměstnaneckých výhod** - více informací naleznete v [Přehledu zaměstnaneckých výhod](hr-benefits-management-overview.md).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Limity prostředí Human Resources jsou nyní založeny na aktualizovaném licencování (394595)

Byl změněn limit počtu prostředí na projekt v rámci Lifecycle Services (LCS). Předchozí limit byl dvě prostředí. Limit pro počet produkčních a sandboxových prostředí, které můžete vytvořit pro Human Resources v LCS, je nyní založen na aktualizovaném licencování. Nyní můžete pro projekt LCS vytvořit tolik prostředí, kolik je třeba, v závislosti na zakoupeném počtu licencí. Nové licencování aktualizované 1. února (2020) umožňuje zákazníkům zakoupit další prostředí. Další informace o licenčních požadavcích pro další prostředí naleznete v tématu [Průvodce licencováním Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Chyba při pokusu o odstranění dotazníku (428603)

Aktualizace tohoto týdne opravuje problém, kdy se při pokusu o odstranění dotazníku zobrazí následující chybová zpráva:

Byla zjištěna nespárovaná dvojice jazyka X + + TTSBEGIN/TTSCOMMIT.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Chyba v deníku výkonu a v zabezpečení odborného certifikátu (428499)

Tato změna omezuje viditelnost deníků výkonu i profesionálních certifikátů na základě společností, ke kterým mají přístup. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>Zkratka pro Quebec a Manitoba (387510)

Počáteční data byla aktualizována tak, aby odrážela správnou zkratku pro Manitoba a Quebec.

## <a name="new-entities-available-in-data-management-framework"></a>Nové entity dostupné v architektuře pro správu dat

K dispozici jsou následující entity. Pokud tyto entity nejsou uvedeny v seznamu entity, použijte možnost **aktualizovat entity** v **Parametrech rozhraní > Nastavení entit > Aktualizovat seznam entit**.

 - Transakce fondu pracovního volna a absence V2
 - Registrace k pracovnímu volnu a absenci V2
 - Úroveň plánu pracovního volna a absence V2
 - Plán pracovního volna a absence V2

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Řešení Dataverse je nyní k dispozici s následujícími změnami:

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
| Nová entita **Pozice** | <ul><li>Přidána položka **Pozice**</li></ul>Nová entity **Pozice** je zahrnuta do Dataverse, ale tentokrát neodkazuje z entit **Pracovní pozice** nebo **Práce**. |

> [!NOTE]
> Finanční dimenze pro pracovní pozice i zaměstnanost poskytují integraci jedním směrem pro aktualizace z modulu Human Resources do Dataverse. Aktualizace finančních dimenzí nejsou v současné době synchronizovány z Dataverse do modulu Human Resources.

Během příštích několika týdnů budou tyto změny entit k dispozici ve všech prostředích. Postup při ruční instalaci nejnovějšího řešení Dataverse pro Human Resources:

1.  Přejděte do [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com).

2.  Vyberte **Prostředí**.

3.  Vyhledjete prostředí, která chcete upgradovat. Prostředí by mělo odpovídat poli **Název prostředí** v sekci **Informace o Dataverse** ve formuláři **O aplikaci** v modulu Human Resources.

4.  Vyberte prostředí pro zobrazení podrobností o prostředí.

5.  Vyberte možnost **Správa řešení** na panelu akcí nahoře. Otevře se nové okno prohlížeče a přejde do **Centra pro správu Dynamics 365** v kontextu vašeho prostředí.

6.  Na seznamu **Řešení** vyberte možnost **Kotva Dynamics 365 Human Resources**.

7.  Chcete-li použít poslední řešení, vyberte možnost **Upgrade**.

## <a name="in-preview"></a>Náhled

## <a name="leave-suspension"></a>Pozastavit pracovní volno

Můžete přerušit pracovní volno a absenci v Human Resources pro zaměstnance. Pozastavením volna se zastaví časové rozlišení volna pro vybrané typy pracovního volna. Pokud k přerušení dojde po zpracování časového rozlišení, pozastavením volna se vytvoří průběžná Úprava zůstatku zaměstnance. Další informace naleznete v části [Přerušení pracovního volna](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Pravidla pro převod do dalšího období

Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období. Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna. Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).

## <a name="coming-soon"></a>Již brzy

## <a name="new-production-release-cadence"></a>Četnost nových vydání

Počínaje dubnem se četnost vydání produktu Human Resources mění z týdenní aktualizace na čtrnáctidenní aktualizaci. Abychom zajistili sbližování s postupy bezpečného nasazení a udržovat ve službě vysoké standardy stability a spolehlivosti, proces nasazení aktualizací služeb do všech regionů bude nyní tvořen dvěma týdny. Dodatečná testování a sledovaní budou zavedena pro ověření úspěšného nasazení v každé fázi procesu. Další informace o četnosti vydání naleznete v tématu [Aktualizace procesu](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Známé problémy

## <a name="employment-detail-entity"></a>Entita Podrobnosti o zaměstnání

Entita **Podrobnosti o zaměstnání** byla aktualizována pomocí následujících polí: **PayFrequency**, **ID kategorie zaměstnání**, **Typ zaměstnání**, **EmploymentType ID** a **tav zaměstnaneckých výhod zaměstnání**. Data nastavení pro tato pole spoléhají na správu výhod, která je povolena ve Správě funkcí. Tato pole v entitě **Podrobností o zaměstnání** by neměla být naplňována ani aktualizována, protože během importu způsobí chyby.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>V některých prostředích nefunguje náhled služby SharePoint

Pokud nefunguje náhled dokumentů uložených ve službě SharePoint, postupujte následujícím způsobem:

1. Ověřte, zda má uživatelský účet Správce přidružen e-mail k záznamu uživatele. Tyto informace můžete zobrazit na stránce **Uživatel**. Není-li e-mail nastaven, je nutné přidat e-mail a poskytovatele pomocí doplňku OData Excel. Ve výchozím nastavení není v návrhu aplikace Excel e-mailová adresa k dispozici. Je nutné upravit návrh aplikace Excel, přidat všechna pole, použít a aktualizovat. Po dokončení těchto kroků můžete aktualizovat účet správce.

2. Poté, co má účet správce přidružen e-mailový účet, přihlaste se k modulu Human Resources s pověřeními správce.

3. Ve službě SharePoint přistupte k příloze a zobrazte náhled dokumentu.

4. Přihlaste se s jiným uživatelským účtem, který má přístup k přílohám, a ověřte, že náhled funguje očekávaným způsobem.

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]