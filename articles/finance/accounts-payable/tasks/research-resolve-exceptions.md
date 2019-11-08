---
title: Prozkoumání/vyřešení výjimek
description: Zásady faktur dodavatele se spouští při zaúčtování faktury dodavatele na stránce Faktura dodavatele, a při otevření stránky s porušením zásad faktury dodavatele.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2f2e7d401e97aeab9dbc74f65e1a0c03eb0c880
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189331"
---
# <a name="researchresolve-exceptions"></a>Prozkoumání/vyřešení výjimek

[!include [task guide banner](../../includes/task-guide-banner.md)]

Zásady faktur dodavatele se spouští při zaúčtování faktury dodavatele na stránce Faktura dodavatele, a při otevření stránky s porušením zásad faktury dodavatele. Můžete také konfigurovat workflow faktury dodavatele tak, aby spustila zásady faktury dodavatele při každém odeslání faktury do workflowu. 

Zásady faktur dodavatele se nevztahují na faktury, které byly vytvořeny v registru faktur a deníku faktur. 

Ověření párování faktur nepoužívá zásady faktur dodavatele, ale namísto toho nastaví údaje na stránce s parametry závazků.

Tento záznam používá ukázkovou společnost USMF. Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky. Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Příprava na vytvoření zásad faktur dodavatele
1. Přejděte do nabídky Závazky > Nastavení > Parametry závazků.
2. Klikněte na kartu Ověření faktury.
3. Zaškrtněte nebo zrušte označení pole Automaticky aktualizovat stav záhlaví faktury.
4. Klepněte na tlačítko OK.
5. V poli Zaúčtovat fakturu s odchylkami: vyberte požadovanou možnost.
6. Zavřete stránku.
7. Přejděte na Závazky > Nastavení zásad > Zásady faktur dodavatele.
8. Klikněte na Parametry.
9. Klepněte na tlačítko btnAdd.
10. Zavřete stránku.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Vytvoření nebo aktualizace typů pro faktury dodavatele
1. Přejděte na Závazky > Nastavení zásad > Typy pravidel zásad pro faktury dodavatele.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název pravidla.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Název dotazu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Klikněte na položku Uložit.
9. Zavřete stránku.

## <a name="define-a-vendor-invoice-policy"></a>Definování zásad faktur dodavatele
1. Přejděte na Závazky > Nastavení zásad > Zásady faktur dodavatele.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. Zadejte nějakou hodnotu do pole Popis.
5. Rozbalte nebo sbalte část Organizace zásad.
6. Ve stromovém zobrazení vyberte systém Contoso Entertainment System USA.
7. Klepněte na možnost Přidat.
8. Rozbalte nebo sbalte část Pravidla zásad.
9. Klikněte na Vytvořit pravidlo zásad.
10. Zadejte hodnotu do pole Popis pravidla zásad.
11. Klepněte na tlačítko Filtr.
12. Klepněte na možnost Přidat.
13. Označte v seznamu vybraný řádek.
14. V poli Tabulka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
15. Klikněte na odkaz na vybraném řádku v seznamu.
16. V poli Odvozená tabulka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
17. Klikněte na odkaz na vybraném řádku v seznamu.
18. V poli Pole kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
19. Zadejte hodnotu do pole Pole.
20. Zavřete stránku.
21. Zadejte hodnotu do pole Kritéria.
22. Klikněte na tlačítko OK.
23. Klikněte na tlačítko OK.
24. Zavřete stránku.
25. Zavřete stránku.
