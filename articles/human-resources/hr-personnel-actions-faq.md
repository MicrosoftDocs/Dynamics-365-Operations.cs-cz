---
title: Často kladené dotazy k akcím personálu
description: Tento článek obsahuje odpovědí na možné otázky, pokud vaše organizace používá akce personálu.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 8882fd00c68dc3cafcb4ecf1b2fe351a9e7f5741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874300"
---
# <a name="personnel-actions-faq"></a>Často kladené dotazy k akcím personálu


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek obsahuje odpovědí na možné otázky, pokud vaše organizace používá akce personálu. Akce personálu jsou další kroky, které je třeba splnit při provádění určité úlohy týkající se personálu. 

Příklady úkolů, které mohou vyžadovat zásah personálu, jsou:
 - Když vytváříte nové pozice. 
 - Upravit existující hodnoty pozice. 
 - Přijmout nové pracovníky. 
 - Převést pracovníky. 
 - Změnit kompenzaci pracovníka. 
 - Změna pozic pracovníka. 
 - Dát pracovníkům výpověď.

> [!NOTE]
> Akce personálu jsou dostupné pouze tehdy, když jsou pole **Povolit akce pracovníka** a **Povolit akce pozice** nastavena na **Ano** na kartě **Akce personálu** na stránce **Sdílené parametry lidských zdrojů**. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Jak lze zjistit, zda organizace vyžaduje akce personálu?
Akce personálu jsou ve vaší organizaci vyžadovány, pokud budete vyzváni k výběru akce personálu při vytváření nových pozic, změnách existujících pozic, náboru nových pracovníků, převodu pracovníků, změně kompenzace pracovníka, změně přiřazení pozic, udělení výpovědi pracovníkům nebo udělení volna pracovníkům. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Jaký je je rozdíl mezi akcí pozice a akcí pracovníka?
Existují dva typy akcí personálu:

- Akce **Pozice** – Akce pozice je provedena u existujících nebo nových pozicí. Akce pozice například může být nutná, pokud měníte hodnotu v existující pozici, nebo pokud vytváříte novou sezónní pozici. 

- Akce **Pracovník** – Akce pracovníka se provádí u existujících zaměstnanců nebo nových zaměstnanců. Akce může být například nutná při přijetí nového zaměstnance nebo při povýšení stávajícího zaměstnance. 

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Co znamenají stavy akcí personálu?
Akce pracovníků mohou mít následující stavy:

- **Koncept** – Pokud je použit workflow, akce nebyla odeslána. Není-li použit workflow, akce nebyla dokončena.
- **Probíhá kontrola** – Akce personálu byla odeslána do workflowu, ale workflow není dokončen.
- **Schválené čekání** – Workflow je dokončen, ale změny budou nadále ve stavu zpracování. **Zrušeno** – Workflow byl zrušen nebo akce personálu byla odvolána. **Zamítnuto** – Žádost o akci byla zamítnuta schvalujícím.
- **Akce zpracování** – Žádost o akci byla schválena a probíhá zpracování změn.
- **Workflow dokončen** – Workflow je dokončen a změny byly zpracovány. **Selhání** – Workflow se nezdařil, protože údaje jsou zastaralé. Klikněte na tlačítko **Znovu aktivovat** pro zobrazení aktuálních informací a pokračování.
- **Dokončeno** – Pozice byla úspěšně vytvořena nebo upravena, nebo byl zaměstnance úspěšně přijat, převeden, propuštěn nebo došlo ke změně jeho kompenzace. **Chyba** – Problém byl způsoben něčím jiným, než je neaktuálnost informace. Otevřete **Protokol zpráv akcí personálu** k zjištění příčiny chyby.
- **Zamítnuto** – Žádost o akci byla odepřena schvalovatelem.

## <a name="can-i-delete-a-personnel-action"></a>Můžu odstranit akci personálu?
Ano, můžete odstranit akce personálu se stavem **Koncept**, **Chyba**, **Selhání** nebo **Zrušeno**. Můžete odstranit akce zaměstnanců, které mají stav **Dokončeno**, pouze pokud jste nastavili možnost **Povolit mazání dokončených akcí pracovníků** na **Ano** na stránce **Sdílené parametry lidských zdrojů**.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Jak mohu nejrychleji zkontrolovat stav žádosti o akci personálu?
Otevřete libovolnou stránku seznamu **Akcí personálu** a vyberte akci personálu.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Co dělat, pokud je žádost o akci personálu neúspěšný?
Pokud požadavek akce personálu selže, postupujte v řešení chyby a opětovném odeslání žádosti:

> 1. Klikněte v **podokně akcí** na tlačítko **Text chyby**, aby se zobrazil text zprávy s popisem problému.
> 
> 2. V **podokně akcí** klikněte na tlačítko **Znovu aktivovat**, abyste načetli nejnovější informace o stavu akce personálu zpět ve stavu **Koncept**.
> 
> 3. Vyřešte chybu a klikněte na možnost **Dokončit** nebo **Odeslat**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Co se stane s akcí personálu používající workflow po dokončení výsledného schválení?
Jestliže nebudou nalezeny žádné chyby, bude akce personálu jen pro čtení. (Historii můžete zobrazit na stránce seznamu **Všechny akce pracovníků**, ale nelze změnit akci personálu.) Pokud je stav akce personálu **Dokončeno**, záznam pozice nebo pracovníka již byl aktualizován. Pokud chcete zobrazit, které změny byly provedeny, otevřete stránku se seznamem **Pozice** nebo **Pracovníci**.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Proč se zobrazuje následující chyba při zadání nenulové hodnoty v poli Mzdová sazba? „Hodnota je mimo platný rozsah – musí být v rozsahu 0,00 až 0,00“
Tato zpráva se zobrazí, protože pole **Úroveň** ve formuláři **Úloha** je prázdná pro úlohu, která je přidružená k vybrané pozici.

Tuto chybu vyřešíte takto:

> 1. Na stránce **Přiřazení pozice pracovníka** klepněte na pole **Pozice**.  
> 2. Klikněte na hodnotu pole **Úloha** pro otevření stránky **Úloha**.
> 3. V podokně akcí klikněte na tlačítko **Upravit**.
> 4. Klikněte na kartu **Kompenzace**.
> 5. V poli **Úroveň** vyberte úroveň.
> 6. Zavřete stránku **Úloha**.
> 7. Zavřete stránku **Pozice**.
> 8. Návrat na kartu **Kompenzace** na stránce **Pracovník** vyberte **Fixní kompenzace**.  Vyberte možnost **Nový** a určete pozici zaměstnance v poli **Pozice**.  Zadejte hodnotu do pole **Plán** a poté zadejte do pole **Sazba mzdy** kompenzaci zaměstnance.

## <a name="why-cant-i-change-the-effective-date-on-the-header-of-the-worker-action-page"></a>Proč nemohu změnit datum platnosti v záhlaví stránky Akce pracovníka?
Datum platnosti nelze změnit, protože pole je vyplněno nejlogičtějším datem pro typ akce.

Příklad:

- Datum platnosti v záhlaví akce **Dát pracovníkovi výpověď** je datum, které jste zadali do pole **Datum výpovědi**.
- Datum platnosti v záhlaví akce **Přijmout pracovníka** je datum, které jste zadali do pole **Počáteční datum zaměstnání**.
- Datum platnosti v záhlaví akce **Převést pracovníka** je datum, které jste zadali do pole **Počáteční datum přiřazení** pro pracovníka.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
