---
title: "Termín vystavení faktury"
description: "Tento článek vysvětluje, jak nastavit parametry pro výpočet dat splatnosti pro vydání faktur dodavatele a faktur odběratele v Evropské unii (EU)."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10923
ms.assetid: 64ea3343-df94-4a52-b839-6328c8a282bd
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 6121be0dd02659e4e8466b0c1381678be64fefc2
ms.lasthandoff: 03/31/2017


---

# <a name="invoice-issue-deadline"></a>Termín vystavení faktury

[!include[banner](../includes/banner.md)]


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
| Související úkoly nastavení | Na stránce **Časové intervaly** nastavte časový interval, který se používá k výpočtu data vystavení faktury. (Klepněte na tlačítko **Finance**&gt;**nastavení financí**&gt;**datum intervalu**.) Na **parametry zahraničního obchodu** stránky, nastavte vlastnosti zahraničního obchodu v různých zemích. (Klepněte na tlačítko **daně**&gt;**nastavení**&gt;**zahraničního obchodu**&gt;**parametry zahraničního obchodu**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>Pravidlo pro výpočet data splatnosti pro vystavení faktury
Můžete použít stránku **Nastavení výpočtu pro datum vystavení faktury** a nastavit pravidlo pro výpočet data vystavení faktury tím, že přiřadíte kód časového intervalu k typu země/oblasti.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Parametry kontroly data pro faktury odběratelů a dobropisy
Můžete nastavit parametry kontroly data, abyste zajistili, že faktury odběratelů a dobropisy pro odběratele jsou generovány během zadaného období po dodání. Tyto parametry v naleznete v části **Kontrola dat faktury** na stránce **Parametry pohledávek**.

## <a name="example"></a>Příklad
Nastavit Microsoft Dynamics 365 pro operace pro výpočet faktury problém data splatnosti pro obchod uvnitř EU dodávky patnáctým dnem měsíce následujícího po doručení dodávky, vytvořte datum intervalu kód a výpočet pravidlo, které mají následující nastavení.

### <a name="date-interval-code"></a>Kód časového intervalu

| Pole                                                           | Hodnota                           |
|-----------------------------------------------------------------|---------------------------------|
| Kód časového intervalu                                              | 15 NM                           |
| Popis                                                     | Patnáctý den následujícího měsíce |
| Před (ve skupině polí **Do data**)                         | Měsíc                           |
| Začátek/Konec (ve skupině polí **Do data**)                      | Konec                             |
| +/- (ve skupině polí **Do data**)                            | září                              |
| Dny, měsíce, roky nebo období (ve skupině polí **Do data**) | Dny                            |

### <a name="invoice-issue-due-date-calculation-rule"></a>Pravidlo pro výpočet data splatnosti pro vystavení faktury

| Pole               | Hodnota                                                     |
|---------------------|-----------------------------------------------------------|
| Typ země/oblasti | **EU**                                                    |
| Počáteční datum          | Zadejte datum, od kterého je aktuální nastavení platné. |
| Kód časového intervalu  | **15-NM**                                                 |

## <a name="next-steps"></a>Další kroky
Po dokončení nastavení parametrů pro výpočet dat splatnosti pro vystavení faktury můžete vytvořit a zaúčtovat následující transakce a automaticky tak vypočítat a aktualizovat data splatnosti pro vystavení faktur:

-   **Prodejní objednávky** – Při vytvoření prodejní objednávky a zaúčtování dodacího listu se vypočítají data splatnosti pro vystavení faktury bude a aktualizují na dodacím listu. Datum splatnosti je vypočítáno na základě v časovém intervalu, který je přidružen země, který je uveden v adrese dodání prodejní objednávky. Po zaúčtování dodacího listu můžete ověřit vydání faktury datum splatnosti v **vydání faktury, datum splatnosti** na **deníku dodacích listů** stránky. (Klepněte na tlačítko **prodeje a marketingu**&gt;**prodeje**&gt;**objednávky dodávky**&gt;**dodací list**.) Všechny dodací listy, které nejsou fakturovány a vydání faktury můžete zobrazit data splatnosti, na **dodací listy, které nebyly fakturovány** stránky. (Klepněte na tlačítko **prodeje a marketingu**&gt;**prodeje**&gt;**objednávka dodávky**&gt;**nefakturované dodací listy**.)
-   **Nákupní objednávky** – Při vytvoření nákupní objednávky a zaúčtování příjemky produktu se vypočítají data splatnosti pro vystavení faktury bude a aktualizují na příjemce produktu. Datum splatnosti je vypočítáno podle časového intervalu, který je přidružen k zemi/regionu určenému v primární adrese dodavatele. Po zaúčtování příjemky produktu můžete zkontrolovat datum vystavení faktury v poli **Datum vystavení faktury** na stránce **Deník příjemek produktů**. (Klepněte na tlačítko **zásobování a zdroje**&gt;**nákupní objednávky**&gt;**příjem produktů**&gt;**příjemky produktu**.) Všechny příjemky produktu, které nejsou fakturovány a vydání faktury můžete zobrazit data splatnosti, na **nefakturované příjemky produktů** stránky. (Klepněte na tlačítko **zásobování a zdroje**&gt;**nákupní objednávky**&gt;**příjem produktů**&gt;**nefakturované příjemky produktů**.)

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
<td>Klepněte na tlačítko <strong>Správa systému</strong>&gt;<strong>nastavení</strong>&gt;<strong>licence</strong>&gt;<strong>konfigurace licence</strong>. Klikněte na konfigurační klíč <strong>Hlavní kniha</strong>.</td>
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






