---
title: Přehled DPH
description: Toto téma podává přehled o systému DPH. Vysvětluje prvky nastavení DPH a jejich společné fungování.
author: ShylaThompson
manager: AnnBe
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16a67ef625fdde0755e96c959be1fb2989ca53b6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770659"
---
# <a name="sales-tax-overview"></a>Přehled DPH

[!include [banner](../includes/banner.md)]

Toto téma podává přehled o systému DPH. Vysvětluje prvky nastavení DPH a jejich společné fungování.

<a name="overview"></a>Přehled
--------

Systém DPH podporuje spoustu typů nepřímých daní, jako daň z prodeje, daň z přidané hodnoty (DPH), daň ze zboží a služeb tax (GST), poplatky jednotkové poplatky a srážková daň. Tyto daně jsou vypočítány a zdokumentovány během transakcí nákupu a prodeje. Musí být pravidelně vykazována a zaplacena finančnímu úřadu. 

Následující diagram znázorňuje entity nastavení daně a jejich propojení.

[![Diagram znázorňující přehled entit nastavení daně](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Pro každou daň z prodeje, kterou společnost musí vykazovat, je třeba definovat kód daně z prodeje. Kód daně z prodeje ukládá sazby daně a pravidla pro výpočet daně z prodeje. 

Každý kód daně z prodeje musí být spojen s obdobím vyrovnání daně z prodeje. Období vyrovnání daně z prodeje definují intervaly, ve kterých musí být daň z prodeje vykázána a zaplacena finančnímu úřadu. Každé období vyrovnání daně z prodeje musí být přiřazeno úřadu pro kontrolu daně z prodeje. Úřad pro kontrolu daně z prodeje představuje entitu, které je daň z prodeje vykázána a zaplacena. Definuje také rozvržení sestavy daně z prodeje. Úřady pro kontrolu daně z prodeje mohou být přiřazeny účtům dodavatelů. Další informace naleznete v tématu [Nastavení období vyrovnání DPH](tasks/set-up-sales-tax-settlement-periods.md).

Každý kód daně z prodeje musí být také spojen se skupinou pro zaúčtování do hlavní knihy. Skupinu pro zaúčtování do hlavní knihy určuje hlavní účty, na které budou zaúčtovány částky pro kódy daně z prodeje. 

Lze také definovat volitelné kódy vykazování daně z prodeje. Ty mohou být přiřazeny ke kódům daně z prodeje pro různé typy částky, které byly vypočteny pro kód daně z prodeje. Sestava **Platba DPH podle kódu** obsahuje součty za kód výkazu daně z prodeje pro dané období a interval vyrovnání daně z prodeje. 

Každá transakce, která vyžaduje výpočet a zaúčtování daně z prodeje, musí mít skupinu daně z prodeje a skupinu daně z prodeje zboží. Skupiny daně z prodeje souvisejí se stranou (například odběratel nebo dodavatele) transakce, zatímco skupiny daně z prodeje zboží se vztahují k prostředku (například zboží nebo kategorie zásobování) transakce. Daňové skupiny obsahují seznam kódů daní. Kódy daně uvedené ve skupině daně z prodeje a skupině daně z prodeje zboží pro transakci jsou kódy daně, které se vztahují na transakci. 

Následující tabulka popisuje entity a posloupnosti nastavení daně.

| Aktivita nastavení                                                  | Požadované nebo Volitelné a popis                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vytvořte hlavní účty.                                           | Požadováno. Dříve, než lze nastavit funkci daně z prodeje, je nutné vytvořit účty hlavní knihy používané společností za účelem platby a zaznamenávání daní.                                                                                                                                                                             |
| Nastavte účetní skupiny hlavní knihy pro DPH.                     | Požadováno. Skupiny pro zaúčtování do hlavní knihy definují hlavní účty pro zaznamenání a platbu daně z prodeje.   Více informací naleznete v tématu [Nastavení účetních skupin pro DPH](tasks/set-up-ledger-posting-groups-sales-tax.md).                                                                                 |
| Nastavte finanční úřady.                                   | Požadováno. Úřady pro kontrolu daně z prodeje jsou entity, kterým musí být daň vykázána a zaplacena.    Další informace naleznete v tématu [Nastavení daňových úřadů](tasks/set-up-sales-tax-authorities.md).                                                                                                                                          |
| Nastavte období vyrovnání daně z prodeje.                            | Požadováno. Období vyrovnání daně z prodeje obsahují informace o tom, kdy a jak často musí být daň z prodeje vykázána a zaplacena. Souvisejí s úřadem pro kontrolu daně z prodeje.                                                                                                                                                       |
| Nastavte kódy vykazování DPH.                               | Volitelné. Kódy vykazování daně z prodeje lze přiřadit ke kódům daně z prodeje za účelem vykazování částek pro několik kódů daně z prodeje v rámci jednoho kódu vykazování daně z prodeje. Další informace naleznete v tématu [Nastavení kódů vykazování DPH](tasks/set-up-sales-tax-reporting-codes.md).                                         |
| Nastavte kódy daně z prodeje.                                         | Požadováno. Kódy daně z prodeje obsahují sazby daně a pravidla pro výpočet všech daní z prodeje. Kódy daně z prodeje souvisejí s obdobím vyrovnání daně z prodeje a skupinou pro zaúčtování do hlavní knihy. Další informace naleznete v tématu [Nastavení kódů DPH](tasks/set-up-sales-tax-codes.md).                                |
| Nastavení skupin DPH.                                        | Požadováno. Skupiny daně z prodeje obsahují seznam prodejních kódů, které se vztahují na stranu (odběratel či dodavatel) transakce. Pro danou transakci průnik kódů daně z prodeje ve skupině daně z prodeje a skupině daně z prodeje zboží určuje kódy daně z prodeje, které se vztahují na danou transakci.                  |
| Nastavte skupiny daně z prodeje zboží.                                   | Požadováno. Skupiny daně z prodeje zboží obsahují seznam prodejních kódů, které platí pro zdroj (produkt, služba a tak dále) transakce. Pro danou transakci průnik kódů daně z prodeje ve skupině daně z prodeje a skupině daně z prodeje zboží určuje kódy daně z prodeje, které se vztahují na danou transakci. Další informace najdete v tématu [Nastavení skupin DPH a skupin DPH položek](tasks/set-up-sales-tax-groups-item-sales-tax-groups.md). |
| Nastavte parametry daně z prodeje na stránkách parametrů aplikace. | Požadováno. Různé oblasti, jako je například hlavní kniha, pohledávky a závazky, musí nastavit parametry pro správný výpočet nepřímých daní. Přestože většina těchto parametrů má výchozí hodnoty, je třeba je upravit podle požadavků jednotlivých společností.                                          |

## <a name="sales-tax-on-transactions"></a>Daň z prodeje v transakcích
Pro každou transakci (řádky dokumentu k prodeji/nákupu, deníky a tak dále) je nutné zadat skupinu daně z prodeje a skupinu daně z prodeje zboží pro výpočet daně z prodeje. Výchozí skupiny jsou uvedeny v hlavních datech (například kategorie odběratel, dodavatel, položky nebo zásobování), ale je-li nutné, lze skupiny v transakcích ručně změnit. Obě skupiny obsahují seznam kódů daně z prodeje a průnik těchto dvou seznamů kódů daně z prodeje určuje seznam platných kódů daně z prodeje pro transakci. 

U každé transakce můžete vyhledat vypočítanou daň z prodeje otevřením stránky **Transakce DPH**. Můžete vyhledávat daň z prodeje pro řádek dokumentu nebo pro celý dokument. U některých dokumentů (například faktura dodavatele a hlavní deníky) můžete upravit vypočítanou daň z prodeje, pokud původní dokument vykazuje odchylky částky.

## <a name="sales-tax-settlement-and-reporting"></a>Vyrovnání a vykazování daně z prodeje
Daň z prodeje musí být vykázána a zaplacena finančním úřadům v daných intervalech (měsíčně, čtvrtletně atd.). Můžete vyrovnat účty daní pro interval a vyrovnat zůstatky na účet vyrovnání daně, jak je uvedeno ve skupinách pro zaúčtování do hlavní knihy. Tato funkce je k dispozici na stránce **Vyrovnat a zaúčtovat DPH**. Je nutné zadat období vyrovnání daně, pro které by měna být vyrovnána DPH. 

Poté, co byla daň z prodeje zaplacena, zůstatky na účtu vyrovnání daně z prodeje by měly být srovnány dle bankovního účtu. Pokud úřad pro kontrolu daně z prodeje, který je uveden v období vyrovnání daně z prodeje, souvisí s účtem dodavatele, zůstatek daně z prodeje bude zaúčtován jako otevřená faktura dodavatele a lze jej zahrnout do návrhu běžné platby.

## <a name="conditional-sales-tax"></a>Nerealizovaná DPH
Podmíněná DPH je DPH, která je vyplacena úměrně ke skutečné částce zaplacené na základě faktury. Naopak standardní DPH se vypočítává v době fakturace. Podmíněná daň DPH musí být odvedena finančnímu úřadu při zaúčtování platby, nikoli při zaúčtování faktury. Při zaúčtování faktury musí být transakce uvedena v sestavě knihu DPH. Transakce však musí být vyloučena ze sestavy platby DPH. 

Pokud zaškrtnete políčko Podmíněná DPH ve formuláři Parametry hlavní knihy, nelze odečíst žádnou DPH, dokud nezaplatíte fakturu. Jedná se o zákonný požadavek v některých zemích / regionech.

> [!NOTE]
> Při zaškrtnutí políčka Podmíněná DPH musíte nastavit kódy DPH a skupiny DPH a vytvořit také skupiny zaúčtování hlavní knihy na podporu této funkce. |

###  <a name="example"></a>Příklad

Vyrovnáváte DPH každý měsíc. 15. června jste vytvořili fakturu zákazníka na částku 10 000 plus DPH.
-   DPH je 25 % nebo 2 500.
-   Datum splatnosti faktury 30. července.

Obvykle je nutné vyrovnat a zaplatí 2 500 finančnímu úřadu při zaúčtování faktury v červnu, i když jste neobdrželi platbu od zákazníka. 

Pokud však používáte podmíněnou DPH, provedete se vyrovnání u finančního úřadu, když obdržíte platbu od zákazníka 30. července.

### <a name="postdated-check"></a>Postdatovaný šek

Pokud použijete postdatovaný šek jako způsob platby, dojde při vytvoření platby k vymazání bankovního účtu. V některých zemích se DPH stane "realizovanou" odpovědností, když se platba zúčtuje v bance, což znamená, že postdatovaný šek je vyrovnán. Můžete ho povolit výběrem možnosti **Realizovat podmíněnou DPH při zaúčtování postdatovaných šeků** v části **Správa hotovosti a banky > Nastavení > Parametry správy hotovosti a banky > Postdatované šeky**.

Další informace naleznete v tématu [Nastavení srážkové daně](tasks/set-up-withholding-tax.md).
