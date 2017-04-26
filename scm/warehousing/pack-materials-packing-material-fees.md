---
title: "Obalové materiály a poplatky"
description: "Poplatky za balicí materiál se recyklační společnosti hradí v určitých intervalech. Platí se částka za hmotnostní jednotku za každý materiál, ze kterého se skládá jednotka balného. Poplatky za balicí materiál jsou vypočítány a vykázány, ale nezaúčtují se žádné nikdy neúčtované transakce, protože poplatky se nepovažují za daně, které je třeba zaplatit úřadům."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 7c0bc5b5d86956336012096c11d0d7621abab1f9
ms.lasthandoff: 03/31/2017


---

# <a name="packing-materials-and-fees"></a>Obalové materiály a poplatky

[!include[banner](../includes/banner.md)]


Poplatky za balicí materiál se recyklační společnosti hradí v určitých intervalech. Platí se částka za hmotnostní jednotku za každý materiál, ze kterého se skládá jednotka balného. Poplatky za balicí materiál jsou vypočítány a vykázány, ale nezaúčtují se žádné nikdy neúčtované transakce, protože poplatky se nepovažují za daně, které je třeba zaplatit úřadům.

Hmotnosti a poplatky za balicí materiály se počítají pro řádky prodejní objednávky i nákupní objednávky.

Pro položku, skupinu položek balení nebo pro všechny položky můžete definovat jednu nebo více jednotek balného. Jednotka balení obsahuje obalové materiály, jejich hmotnost a počet jednotek, které jsou obsaženy v jednotce balení. Kód obalového materiálu je přiřazen ke každému definovanému typu obalového materiálu. Na základě kódu obalového materiálu můžete stanovit cenu za určité období. Poplatku za obalový materiál je počítán na základě těchto informací.

| **Poznámka **                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| I když vaše společnost neplatí poplatky za obalový materiál, lze funkci použít ke statistickým výpočtům hmotností obalového materiálu. |

## <a name="setup-requirements-for-packing-material-fees"></a>Nastavení požadavků pro poplatky za obalový materiál
Dříve než začnete počítat hmotnosti obalových materiálů, poplatky za obalové materiály nebo obě tyto hodnoty, je nutné vytvořit tato základní data:

-   Skupiny balení – Vytvořte skupiny balení, které se budou přiřazovat položkám.
-   Kódy obalového materiálu – Pro každý typ definovaného obalového materiálu vytvořte kód obalového materiálu.
-   Jednotky balení – Určete jednotku balení pro položku, pro skupinu balení nebo pro všechny položky. U každé jednotky balného určete, které obalové materiály zahrnout, přiřaďte hmotnosti a v poli Koeficient jednotky balení zadejte koeficient převodu ze skladových jednotek.
-   Poplatky za obalový materiál – Určete poplatky za obalový materiál pro každý kód obalového materiálu. Pro každý typ materiálu určete dobu platnosti, cenu za materiál, měnu a jednotku.

## <a name="packing-units-on-sales-order-lines"></a>Jednotky balení na řádcích prodejní objednávky
Při vytvoření řádku prodejní objednávky systém zkontroluje, zda jsou pro položku určeny jednotky balení. Jsou-li jednotky balení určeny, systém aktualizuje řádek prodejní objednávky o příslušnou jednotku balení a množství jednotky balení. Množství jednotky balení vychází z objednaného množství, které se vydělí počtem položek vybrané jednotky balení. Pokud nebyla stanovena jednotka balení, lze jednotku balení a množství jednotky balení na řádku prodejní objednávky zadat ručně. Při zaúčtování řádku prodejní objednávky lze rovněž změnit jednotku balení a množství jednotky balení. To má význam v případě, kdy je řádek prodejní objednávky částečně doručen nebo fakturován. Při fakturaci prodejní objednávky se vytvoří transakce obalového materiálu. Transakce obalového materiálu obsahuje hmotnost obalového materiálu pro řádky prodeje. Transakce lze upravit rovněž po jejich fakturaci a poté vytvořit nové transakce.

## <a name="packing-units-on-purchase-order-lines"></a>Jednotky balení na řádcích nákupní objednávky
Transakce obalového materiálu pro řádek nákupní objednávky nejsou systémem vytvářeny. Na stránce **Transakce obalového materiálu** můžete ručně vytvořit transakce pro fakturované řádky nákupní objednávky.

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a>Nastavit licenční čísla packagingmaterialfee
Pokud odběratelé platí poplatky za obalový materiál, zadejte licenční čísla poplatku za obalový materiál odběratelů na stránce **Odběratelé**. Po přiřazení licenčního čísla odběrateli se při fakturování prodejních objednávek automaticky vypočítávají poplatky za obalový materiál. Po fakturování se označení zaškrtávacího políčka **Vypočítat poplatek** na stránce **Transakce obalového materiálu** zruší, protože není nutné vypočítávat a tisknout sestavu. Na faktuře můžete vytisknout hmotnosti obalového materiálu a informovat odběratele, že platí poplatky. 

Pokud vaše společnost platí poplatky za obalový materiál, nezadávejte licenční čísla odběratelů. Po vyfakturování se označí zaškrtávací políčko **Vypočítat poplatek** na stránce **Transakce obalového materiálu**. To znamená, že se poplatky vypočítají při vytvoření sestavy. Na faktuře můžete vytisknout hmotnosti a informovat o tom, že poplatky za obalový materiál platí vaše společnost.

## <a name="print-packaging-material-weights-on-invoices"></a>Tisk hmotností obalového materiálu na fakturách
Na faktuře můžete vytisknout hmotnosti obalového materiálu a informovat o tom, kdo platí poplatky za obalový materiál. Hmotnosti se sčítají pro jednotlivé kódy obalu.
 





