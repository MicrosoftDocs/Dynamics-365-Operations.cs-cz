---
title: "Výkaz DPH pro Českou republiku"
description: "Nastavení a generování výkazu DPH pro uživatele v právnických osobách, které jsou umístěny v České republice."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxReportVoucher, TaxTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 263614
ms.assetid: eef73389-e480-451d-a43d-562429b41742
ms.search.region: Czech Republic
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a8426fffb3f2cbc9373c484bb4072904c676b8a8
ms.lasthandoff: 03/31/2017


---

# <a name="vat-statement-for-the-czech-republic"></a>Výkaz DPH pro Českou republiku

[!include[banner](../includes/banner.md)]


Nastavení a generování výkazu DPH pro uživatele v právnických osobách, které jsou umístěny v České republice.

Toto téma obsahuje informace specifické pro zemi o nastavení výkazu DPH pro uživatele v právnických osob v České republice. Další informace o obecné vykazování DPH, viz [vykazování DPH](emea-vat-reporting.md).

## <a name="set-up-sales-tax-authorities"></a>Nastavení daňových úřadů
Požadovaný formát pro konkrétní finanční úřad generovat přiznání k DPH, musíte vytvořit rozložení sestavy pro finanční úřady.

-   Na **finančnímu úřadu** stránky v **Obecné** oddíl, nastavte ** rozložení sestavy ** na **výchozí**.
-   Vyberte stejné **finančnímu úřadu** u **období vyrovnání DPH** používaný pro kódy DPH.

## <a name="set-up-sales-tax-reporting-codes"></a>Nastavit kódy vykazování DPH
Následuje příklad nastavení může kódy vykazování DPH pro generování výkazu DPH.

### <a name="example"></a>Příklad

Pro uživatele v právnických osob v České republice, podle prohlášení DPH 2016, nelze vytvořit následující kódy vykazování DPH.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| **Sales tax reporting code** | **Description**                                         |
| 2101                         | Ř.210 - se zákl. Sazbou daně - Základ                  |
| 2102                         | Ř.210 - se zákl. Sazbou daně - Daň                     |
| 2151                         | Ř.215 - se sníž. Sazbou daně - Základ                  |
| 2152                         | Ř.215 - se sníž. Sazbou daně - Daň                     |
| 2201                         | Ř.220 - se zákl. Sazbou daně - Základ                  |
| 2202                         | Ř.220 - se zákl. Sazbou daně - Daň                     |
| 2251                         | Ř.225 - se sníž. Sazbou daně - Základ                  |
| 2252                         | Ř.225 - se sníž. Sazbou daně - Daň                     |
| 2301                         | Ř.230 - se zákl. Sazbou daně - Základ                  |
| 2302                         | Ř.230 - se zákl. Sazbou daně - Daň                     |
| 2351                         | Ř.235 - se sníž. Sazbou daně – Základ                   |
| 2352                         | Ř.235 - se sníž. Sazbou daně – Daň                      |
| 2401                         | Ř.240 - se zákl. Sazbou daně - Základ                  |
| 2402                         | Ř.240 - se zákl. Sazbou daně - Daň                     |
| 2451                         | Ř.245 - se sníž. Sazbou daně - Základ                  |
| 2452                         | Ř.245 - se sníž. Sazbou daně - Daň                     |
| 2501                         | Ř.250 - běžná cena od osob V jiném čl.státě - Základ          |
| 2502                         | Ř.250 - běžná cena od osob V jiném čl.státě - Daň             |
| 2551                         | Ř.255 - od osob nereg. V jiném čl.státě - Základ        |
| 2552                         | Ř.255 - od osob nereg. V jiném čl.státě - Daň           |
| 2601                         | Ř.260 - se zákl. Sazbou daně – Základ                   |
| 2602                         | Ř.260 - se zákl. Sazbou daně – Daň                      |
| 2651                         | Ř.265 - se sníž. Sazbou daně – Základ                   |
| 2652                         | Ř.265 - se sníž. Sazbou daně - Daň                      |
| 2701                         | Ř.270 - se zákl. Sazbou daně - Základ                  |
| 2702                         | Ř.270 - se zákl. Sazbou daně - Daň                     |
| 2751                         | Ř.275 - se sníž. Sazbou daně - Základ                  |
| 2752                         | Ř.275 - se sníž. Sazbou daně - Daň                     |
| 3101                         | Ř.310 - se zákl. Sazbou daně - Základ                   |
| 3102                         | Ř.310 - se zákl. Sazbou daně - Daň, plný nárok          |
| 3103                         | Ř.310 - se zákl. Sazbou daně - Daň, krác. nárok         |
| 3151                         | Ř.315 - se sníž. Sazbou daně - Základ                   |
| 3152                         | Ř.315 - se sníž. Sazbou daně - Daň, plný nárok          |
| 3153                         | Ř.315 - se sníž. Sazbou daně - Daň, krác. nárok         |
| 3201                         | Ř.320 - se zákl. Sazbou daně - Základ                  |
| 3202                         | Ř.320 - se zákl. Sazbou daně - Daň, plný nárok         |
| 3203                         | Ř.320 - se zákl. Sazbou daně - Daň, krác. nárok        |
| 3251                         | Ř.325 - se sníž. Sazbou daně - Základ                  |
| 3252                         | Ř.325 - se sníž. Sazbou daně - Daň, plný nárok         |
| 3253                         | Ř.325 - se sníž. Sazbou daně - Daň, krác. nárok        |
| 3301                         | Ř.330 - se zákl. Sazbou daně - Základ                   |
| 3302                         | Ř.330 - se zákl. Sazbou daně - Daň, plný nárok          |
| 3303                         | Ř.330 - se zákl. Sazbou daně - Daň, krác. nárok         |
| 3351                         | Ř.335 - se sníž. Sazbou daně - Základ                  |
| 3352                         | Ř.335 - se sníž. Sazbou daně - Daň, plný nárok         |
| 3353                         | Ř.335 - se sníž. Sazbou daně - Daň, krác. nárok        |
| 3401                         | Ř.340 - se zákl. Sazbou daně - Základ                   |
| 3402                         | Ř.340 - se zákl. Sazbou daně - Daň, plný nárok          |
| 3403                         | Ř.340 - se zákl. Sazbou daně - Daň, krác. nárok         |
| 3451                         | Ř.345 - se sníž. Sazbou daně - Základ                  |
| 3452                         | Ř.345 - se sníž. Sazbou daně - Daň, plný nárok         |
| 3453                         | Ř.345 - se sníž. Sazbou daně - Daň, krác. nárok        |
| 3501                         | Ř.350 - se zákl. Sazbou daně - Základ                  |
| 3502                         | Ř.350 - se zákl. Sazbou daně - Daň, plný nárok         |
| 3503                         | Ř.350 - se zákl. Sazbou daně - Daň, krác. nárok        |
| 3551                         | Ř.355 - se sníž. Sazbou daně - Základ                  |
| 3552                         | Ř.355 - se sníž. Sazbou daně - Daň, plný nárok         |
| 3553                         | Ř.355 - se sníž. Sazbou daně - Daň, krác. nárok        |
| 3601                         | Ř.360 - běžná cena od osob V jiném čl.státě - Základ          |
| 3602                         | Ř.360 - běžná cena od osob V jiném čl.státě - Daň             |
| 3603                         | Ř.360 - běžná cena od osob V jiném čl.státě - Daň, krác.      |
| 3651                         | Ř.365 - od osob nereg. V jiném čl.státě - Základ        |
| 3652                         | Ř.365 - od osob nereg. V jiném čl.státě - Daň           |
| 3653                         | Ř.365 - od osob nereg. V jiném čl.státě - Daň, kr.      |
| 3702                         | Ř.370 - při změně režimu - Daň, plný nárok             |
| 3703                         | Ř.370 - při změně režimu - Daň, krác. nárok            |
| 3803                         | Ř.380 - celková suma pro krácení nároku na odpočet daně |
| 3902                         | Ř.390 - celková suma plného nároku na odpočet daně      |
| 4102                         | Ř.410 - dodání zboží jiného čl.státu                 |
| 4202                         | Ř.420 - dodání nového dopr.prostř. Osobě reg.           |
| 4252                         | Ř.425 - dodání nového dopr. prostř. Osobě nereg.        |
| 4302                         | Ř.430 - vývoz zboží (§66)                               |
| 4402                         | Ř.440 - Ost.plnění osv.od daně s nárok. Na odpočet      |
| 5102                         | Ř.510 - Celk. usk.plnění s nárokem na odpočet daně      |
| 5202                         | Ř.520 - Uskut. Plnění, která se nezapoč. To koef.       |
| 5302                         | Ř.530 - Celk. osv.usk.plnění bez nároku na odpočet      |
| 5402                         | Ř.540 - Usk.plnění nezapoč. Výpočtu koeficientu      |
| 5503                         | Ř.550 - Vypočt. poměr.část odp.daně (§76) - Koef.       |
| 5502                         | Ř.550 - Vypočt. poměr.část odp.daně (§76)               |
| 5603                         | Ř.560 - Vypoř. odp. Daně (§76 odst.7-10) - Koef.        |
| 5602                         | Ř.560 - Vypoř. odp. Daně (§76 odst.7-10)                |
| 5702                         | Ř.570 - Úprava odpočtu daně (§78)                       |
| 5802                         | Ř.580 - Vyrovnání odpočtu daně (§79)                    |
| 6002                         | Ř.600 - Vrácení daně                                    |
| 7102                         | Ř.710 - Vypořádání daně na výstupu (§91)                |
| 7302                         | Ř.730 - Daň na výstupu                                  |
| 7502                         | Ř.750 - Odpočet daně                                    |
| 7532                         | Ř.753 - Vlastní daňová povinnost                        |
| 7542                         | Ř.754 - Nadměrný odpočet                                |
| 7802                         | Ř.780 - Změna daň.povinnosti při podání dod. přiz.      |
| 8101                         | Ř.810 - Pořízení zboží prostřední osobou                |
| 8151                         | Ř.815 - Dodání zboží prostřední osobou                  |

## <a name="configure-the-er-model-and-format-for-the-report"></a>Konfigurace modelu ER a formát sestavy
Lze použít **elektronických sestav** pracovního prostoru, chcete-li zkontrolovat nebo změnit konfiguraci výkazu DPH. Přejděte **konfigurace** stránku a vyberte **model prohlášení DPH** ze seznamu modelů. Tento model je společný pro Rakousko, České republiky, Estonska, Finska, Lotyšska a Litvy a jeho agreguje daně údaje potřebné pro přiznání k DPH. Chcete-li zkontrolovat nebo změnit formát výkazu DPH pro uživatele v právnických osob v České republice, vyberte **přiznání k DPH (CZ)**, který je podřízený **model prohlášení DPH** ve stromu modelu. Vyberte ji a klepněte na tlačítko **Designer** v podokně akcí zobrazit nebo změnit formát. Další informace naleznete v tématu [elektronických sestav.](/dynamics365/operations/dev-itpro/analytics/general-electronic-reporting)

## <a name="generate-the-vat-statement"></a>Generovat výkaz DPH
Chcete-li generovat soubor XML DPH, otevřete **platby DPH** stránky, vyberte doklady a potom klepněte na tlačítko **Export DPH do souboru XML**.




