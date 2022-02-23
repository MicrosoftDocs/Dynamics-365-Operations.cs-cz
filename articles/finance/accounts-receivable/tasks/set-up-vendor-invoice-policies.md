---
title: Nastavení zásad faktur dodavatele
description: Toto téma vysvětluje, jak nastavit zásady pro fakturu dodavatele.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58518f5291b70c63506c20717034daff0268901b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441175"
---
# <a name="set-up-vendor-invoice-policies"></a>Nastavení zásad faktur dodavatele

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak nastavit zásady pro fakturu dodavatele. Zásady faktur dodavatele se spouští při zaúčtování faktury dodavatele na stránce Faktura dodavatele, a při otevření stránky s porušením zásad faktury dodavatele. Můžete také konfigurovat workflow faktury dodavatele tak, aby spustila zásady faktury dodavatele při každém odeslání faktury do workflowu. 

- Zásady faktur dodavatele se nevztahují na faktury, které byly vytvořeny v registru faktur a deníku faktur.  
- Ověření párování faktur nepoužívá zásady faktur dodavatele, ale namísto toho nastaví údaje na stránce s parametry závazků.  
- Tento záznam používá ukázkovou společnost USMF. Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky. Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Příprava na vytvoření zásad faktur dodavatele
1. Přejděte na **Navigační podokno > Moduly > Závazky > Nastavení > Parametry závazků**.
2. Zvolte kartu **Ověření faktury**.
3. Zaškrtněte nebo zrušte označení pole **Automaticky aktualizovat stav záhlaví faktury**.
4. Vyberte **OK**.
5. V poli **Zaúčtovat fakturu s odchylkami** vyberte požadovanou možnost.
6. Zavřete stránku.
7. Přejděte na **Navigační podokno > Moduly > Závazky > Nastavení zásad > Zásady faktur dodavatele**.
8. Vyberte **Parametry**.
9. Vyberte **přidat**.
10. Zavřete stránku a vraťte se na domovskou stránku.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Vytvoření nebo aktualizace typů pro faktury dodavatele
1. Přejděte na **Navigační podokno > Moduly > Závazky > Nastavení zásad > Typy zásad faktur dodavatele**.
2. Zvolte **Nové**.
3. Zadejte hodnoty do polí **Název pravidla** a **Popis**.
4. V poli **Název dotazu** klepnutím na rozevírací tlačítko otevřete vyhledávání a poté vyberte požadovaný záznam.
5. Zvolte **Uložit**.
6. Zavřete stránku a vraťte se na domovskou stránku.

## <a name="define-a-vendor-invoice-policy"></a>Definování zásad faktur dodavatele
1. Přejděte na **Navigační podokno > Moduly > Závazky > Nastavení zásad > Zásady faktur dodavatele**.
2. Zvolte **Nové**.
3. Zadejte hodnoty do polí **Název** a **Popis**.
4. Rozbalte nebo sbalte část **Organizace zásad**.
5. Ve stromovém zobrazení vyberte **Contoso Entertainment System USA**.
6. Vyberte **přidat**.
7. Rozbalte nebo sbalte část **Pravidla zásad**.
8. Vyberte **Vytvořit pravidlo zásad**.
9. Zadejte hodnotu do pole **Popis pravidla zásad**.
10. Vyberte **Filtr**.
11. Vyberte **přidat**. Vyberte požadovaný záznam.
12. V polích **Tabulka**, **Odvozená tabulka** a **Pole** vyberte nebo zadejte možnosti z rozevíracích nabídek.
13. Zavřete stránku.
14. Zadejte hodnotu do pole **Kritéria**.
15. Vyberte **OK**.
16. Vyberte **OK**.
17. Zavřete stránky a vraťte se na domovskou stránku.

