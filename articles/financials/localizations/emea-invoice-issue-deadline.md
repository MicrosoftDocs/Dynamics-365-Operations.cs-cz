---
title: Termín vystavení faktury
description: Tento článek vysvětluje, jak nastavit parametry pro výpočet dat splatnosti pro vydání faktur dodavatele a faktur odběratele v Evropské unii (EU).
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10923
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 942b48170d7c164e16d2b8f5544b8777668adab3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549079"
---
# <a name="invoice-issue-deadline"></a>Termín vystavení faktury

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak nastavit parametry pro výpočet dat splatnosti pro vydání faktur dodavatele a faktur odběratele v Evropské unii (EU).

Směrnice Evropské unie (EU) 45/2010 a další směrnice vyžadují, aby se dodávky v EU (dodávky v rámci EU) fakturovaly nejpozději patnáctého dne v měsíci následujícím po měsíci dodání. Jednotlivé země EU mohou mít zároveň různé termíny fakturace pro domácí dodávky. Funkce Termín vystavení faktury vám umožní sjednotit časový interval s typem země/oblasti. Pro všechny dodávky do země/oblasti určitého typu a z ní je datum pro vystavení faktury vypočteno pomocí pravidel, která jsou nastavena v zadaném intervalu. Dále můžete získat všechny dodací listy, které mají určité datum pro vystavení faktury, filtrovat podle data pro vystavení faktury během periodického fakturování prodejů a řídit datum pro vystavení prodejní faktury při zaúčtování faktury. Můžete nastavit kód datového intervalu a nastavit výpočetní pravidlo pro datum výdeje faktury přiřazením kódu datového intervalu k typu země/oblasti. Pravidlo pro výpočet se používá k výpočtu data splatnosti pro vystavení faktur pro následující transakce:

-   Dodávky v rámci EU
-   Domácí dodávky v rámci členského státu EU

Můžete také nastavit řízení dat a pomoci tak zajistit, aby transakce využívající faktury odběratelů a dobropisy pro odběratele byly generovány během zadaného období po dodání.

## <a name="prerequisites"></a>Požadavky
Následující tabulka zobrazuje požadavky, které musí být splněny před použitím funkce datum vystavení faktury.

| Kategorie            | Předpoklad                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Země / oblast      | Primární adresa právnické osoby musí být v členském státě EU.                                                                                                                                                                                                                                                                                                                    |
| Související úkoly nastavení | Na stránce **Časové intervaly** nastavte časový interval, který se používá k výpočtu data vystavení faktury. (Klikněte na položky **Hlavní kniha** &gt; **Nastavení knihy** &gt; **Intervaly data**.) Na stránce **Parametry zahraničního obchodu** nastavte vlastnosti zahraničního obchodu pro různé země / oblasti. (Klikněte na **Daň** &gt; **Nastavení** &gt; **Zahraniční obchod** &gt; **Parametry zahraničního obchodu**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>Pravidlo pro výpočet data splatnosti pro vystavení faktury
Můžete použít stránku **Nastavení výpočtu pro datum vystavení faktury** a nastavit pravidlo pro výpočet data vystavení faktury tím, že přiřadíte kód časového intervalu k typu země/oblasti.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Parametry kontroly data pro faktury odběratelů a dobropisy
Můžete nastavit parametry kontroly data, abyste zajistili, že faktury odběratelů a dobropisy pro odběratele jsou generovány během zadaného období po dodání. Tyto parametry v naleznete v části **Kontrola dat faktury** na stránce **Parametry pohledávek**.

## <a name="example"></a>Příklad
Chcete-li nastavit aplikaci Microsoft Dynamics 365 for Finance and Operations tak, aby počítala data vystavení faktur při dodávce v rámci EU vždy patnáctý den měsíce následujícího po dodání, vytvořte kód datového intervalu a pravidlo pro výpočet s následujícími parametry.

### <a name="date-interval-code"></a>Kód časového intervalu

| Pole                                                           | Hodnota                           |
|-----------------------------------------------------------------|---------------------------------|
| Kód časového intervalu                                              | 15-NM                           |
| Popis                                                     | Patnáctý den následujícího měsíce |
| Před (ve skupině polí **Do data**)                         | Měsíc                           |
| Začátek/Konec (ve skupině polí **Do data**)                      | Konec                             |
| +/- (ve skupině polí **Do data**)                            | 15                              |
| Dny, měsíce, roky nebo období (ve skupině polí **Do data**) | Dny                            |

### <a name="invoice-issue-due-date-calculation-rule"></a>Pravidlo pro výpočet data splatnosti pro vystavení faktury

| Pole               | Hodnota                                                     |
|---------------------|-----------------------------------------------------------|
| Typ země/oblasti | **EU**                                                    |
| Počáteční datum          | Zadejte datum, od kterého je aktuální nastavení platné. |
| Kód časového intervalu  | **15-NM**                                                 |

## <a name="next-steps"></a>Další kroky
Po dokončení nastavení parametrů pro výpočet dat splatnosti pro vystavení faktury můžete vytvořit a zaúčtovat následující transakce a automaticky tak vypočítat a aktualizovat data splatnosti pro vystavení faktur:

-   **Prodejní objednávky** – Při vytvoření prodejní objednávky a zaúčtování dodacího listu se vypočítají data splatnosti pro vystavení faktury bude a aktualizují na dodacím listu. Datum splatnosti je vypočítáno podle časového intervalu, který je přidružen k zemi / oblasti, která je určena v adrese dodání na prodejní objednávce. Po zaúčtování příjemky produktu můžete zkontrolovat datum vystavení faktury v poli **Datum vystavení faktury** na stránce **Deník dodacích listů**. (Klikněte na tlačítko **Prodej a marketing** &gt; **Prodejní objednávka** &gt; **Dopravné objednávky** &gt; **Dodací list**.) Můžete zobrazit všechny dodací listy, které nejsou fakturovány, a jejich data vystavení faktury, na stránce **Nefakturované dodací listy**. (Klikněte na nabídku **Prodeje a marketing** &gt; **Prodejní objednávka** &gt; **Dopravné objednávky** &gt; **Nefakturované dodací listy**.)
-   **Nákupní objednávky** – Při vytvoření nákupní objednávky a zaúčtování příjemky produktu se vypočítají data splatnosti pro vystavení faktury bude a aktualizují na příjemce produktu. Datum splatnosti je vypočítáno podle časového intervalu, který je přidružen k zemi/regionu určenému v primární adrese dodavatele. Po zaúčtování příjemky produktu můžete zkontrolovat datum vystavení faktury v poli **Datum vystavení faktury** na stránce **Deník příjemek produktů**. (Klepněte na **Zásobování a zdroje** &gt; **Nákupní objednávky** &gt; **Příjem produktů** &gt; **Příjemky produktu**.) Na stránce **Nefakturované příjemky produktů** můžete zobrazit všechny příjemky produktů, které nejsou fakturovány, a jejich data vystavení faktury. (Klikněte na nabídku **Zásobování a zdroje** &gt; **Nákupní objednávky** &gt; **Příjem produktů** &gt; **Nefakturované příjemky produktů**.)

## <a name="technical-information-for-system-administrators"></a>Technické informace pro správce systému
Pokud nemáte přístup ke stránkám, které se používají k dokončení úkolů uvedených v tomto článku, obraťte se na správce systému a poskytněte informace, které jsou uvedeny v následující tabulce.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorie</th>
<th>Předpoklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Configuration Keys</td>
<td>Klikněte na <strong>Správa systému</strong> &gt; <strong>Nastavení</strong> &gt; <strong>Licencování</strong> &gt; <strong>Konfigurace licence</strong>. Klikněte na konfigurační klíč <strong>Hlavní kniha</strong>.</td>
</tr>
<tr class="even">
<td>Role a funkční oprávnění zabezpečení</td>
<td>Chcete-li provést tento úkol, musíte být členem role zabezpečení zahrnující následující povinnosti:
<ul>
<li><strong>CustInvoiceInvoiceAndCashProcessEnable</strong> (povolení zpracování faktur a hotovosti)</li>
<li><strong>VendInvoiceInvoicePaymentProcessEnable</strong> (povolení zpracování faktur a platby)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Role a oprávnění zabezpečení</td>
<td>Chcete-li provést tento úkol, musíte být členem role zabezpečení zahrnující následující oprávnění:
<ul>
<li><strong>CustPackingSlipJournalView</strong> (zobrazení prodejních dodacích listů)</li>
<li><strong>VendPackingSlipJournalView</strong> (zobrazení deníku s příjemkou produktu z nákupní objednávky)</li>
<li><strong>LedgerInvoiceIssueDueDateSetupMaintain_W</strong> (výpočet data splatnosti pro vystavení faktury)</li>
</ul></td>
</tr>
</tbody>
</table>





