---
title: Prozkoumání nebo vyřešení výjimek
description: Zásady faktur dodavatele se spouští při zaúčtování faktury dodavatele na stránce Faktura dodavatele, a při otevření stránky s porušením zásad faktury dodavatele.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ff53198f61e1d1af3c437e9488c2a246cf820a
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2022
ms.locfileid: "8110012"
---
# <a name="research-or-resolve-exceptions"></a>Prozkoumání nebo vyřešení výjimek

[!include [banner](../../includes/banner.md)]

Zásady faktur dodavatele se spouští při zaúčtování faktury dodavatele na stránce **Faktura dodavatele**, a při otevření stránky **Porušení zásad** faktury dodavatele. Můžete také konfigurovat workflow faktury dodavatele tak, aby spustila zásady faktury dodavatele při každém odeslání faktury do workflowu. 

Zásady faktur dodavatele se nevztahují na faktury, které byly vytvořeny v **registru faktur** a **deníku faktur**. 

Ověření párování faktur nepoužívá zásady faktur dodavatele, ale namísto toho nastaví údaje na stránce **Parametry závazků**.

Tento záznam používá ukázkovou společnost USMF. Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky. Před prvním krokem ověřte, že je vybraný klíč **Konfigurace párování faktur**.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Příprava na vytvoření zásad faktur dodavatele
1. Přejděte do nabídky **Závazky > Nastavení > Parametry závazků**
2. Klikněte na kartu **Ověření faktury**.
3. Zaškrtněte nebo zrušte označení pole **Automaticky aktualizovat stav záhlaví faktury**.
4. Klikněte na tlačítko **OK**.
5. V poli **Zaúčtovat fakturu s odchylkami** vyberte požadovanou možnost.
6. Zavřete stránku.
7. Přejděte na **Závazky > Nastavení zásad > Zásady faktur dodavatele**.
8. Klikněte na **Parametry**.
9. Klepněte na možnost **Přidat**.
10. Zavřete stránku.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Vytvoření nebo aktualizace typů pro faktury dodavatele
1. Přejděte na **Závazky > Nastavení zásad > Typy pravidel zásad pro faktury dodavatele**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Název pravidla**.
4. Zadejte hodnotu do pole **Popis**.
5. V poli **Název dotazu** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Klikněte na tlačítko **Uložit**.
9. Zavřete stránku.

## <a name="define-a-vendor-invoice-policy"></a>Definování zásad faktur dodavatele
1. Přejděte na **Závazky > Nastavení zásad > Zásady faktur dodavatele**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Název**.
4. Zadejte hodnotu do pole **Popis**.
5. Rozbalte nebo sbalte část **Organizace zásad**.
6. Ve stromovém zobrazení vyberte systém Contoso Entertainment System USA.
7. Klepněte na možnost **Přidat**.
8. Rozbalte nebo sbalte část **Pravidla zásad**.
9. Klikněte na **Vytvořit pravidlo zásad.**
10. Zadejte hodnotu do pole **Popis pravidla zásad**.
11. Klikněte na tlačítko **Filtr**.
12. Klepněte na možnost **Přidat**.
13. Označte v seznamu vybraný řádek.
14. V poli **Tabulka** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
15. Klikněte na odkaz na vybraném řádku v seznamu.
16. V poli **Odvozená tabulka** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
17. Klikněte na odkaz na vybraném řádku v seznamu.
18. V poli **Pole** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
19. Zadejte hodnotu do pole **Pole**.
20. Zavřete stránku.
21. Zadejte hodnotu do pole **Kritéria**.
22. Klikněte na tlačítko **OK**.
23. Klikněte na tlačítko **OK**.
24. Zavřete stránku.
25. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
