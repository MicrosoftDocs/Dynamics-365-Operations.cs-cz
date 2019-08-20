---
title: Výkaz DPH pro Českou republiku
description: Nastavení a generování výkazu DPH pro uživatele v rolích právnických osob na území České republiky.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxReportCollection, TaxReportVoucher, TaxTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 263614
ms.search.region: Czech Republic
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e061b68592ae178ce82f9513c5ca45421c0f182a
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852297"
---
# <a name="vat-statement-for-the-czech-republic"></a>Výkaz DPH pro Českou republiku

[!include [banner](../includes/banner.md)]

Nastavení a generování výkazu DPH pro uživatele v rolích právnických osob na území České republiky.

Toto téma obsahuje informace o nastavení výkazu DPH pro uživatele ve funkcích právnických osob v České republice specifické pro tuto zemi. Další obecné informace o obecném vykazování DPH naleznete v tématu [Vykazování DPH](emea-vat-reporting.md).

## <a name="set-up-sales-tax-authorities"></a>Nastavení daňových úřadů
Pokud chcete generovat deklaraci DPH v požadovaném formátu pro konkrétní daňový úřad, je nutné nastavit rozložení sestavy pro daňové úřady.

- Na stránce <strong>Finanční úřady</strong> v části <strong>Obecné</strong> nastavte <strong>Rozložení sestavy **na **Výchozí</strong>.
- Vyberte **Finanční úřad** pro **Období vyrovnání DPH**, které použijete pro kódy DPH.

## <a name="set-up-sales-tax-reporting-codes"></a>Nastavit kódy vykazování DPH
Následující příklad uvádí, jak by bylo možné nastavit kódy vykazování DPH pro generování výkazu DPH.

### <a name="example"></a>Příklad

Pro uživatele ve funkci právnických osob v České republice je na základě prohlášení o DPH 2016 možné vytvářet následující kódy vykazování DPH.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| **Kód vykazování DPH** | **Popis**                                         |
| 2101                         | Ř.210 - se zákl. sazbou daně - Základ                  |
| 2102                         | Ř.210 - se zákl. sazbou daně - Daň                     |
| 2151                         | ř.215 - se sníž. sazbou daně - Základ                  |
| 2152                         | ř.215 - se sníž. sazbou daně - Daň                     |
| 2201                         | ř.220 - se zákl. sazbou daně - Základ                  |
| 2202                         | ř.220 - se zákl. sazbou daně - Daň                     |
| 2251                         | ř.225 - se sníž. sazbou daně - Základ                  |
| 2252                         | ř.225 - se sníž. sazbou daně - Daň                     |
| 2301                         | ř.230 - se zákl. sazbou daně - Základ                  |
| 2302                         | ř.230 - se zákl. sazbou daně - Daň                     |
| 2351                         | ř.235 - se sníž. sazbou daně – Základ                   |
| 2352                         | ř.235 - se sníž. sazbou daně – Daň                      |
| 2401                         | ř.240 - se zákl. sazbou daně - Základ                  |
| 2402                         | ř.240 - se zákl. sazbou daně - Daň                     |
| 2451                         | ř.245 - se sníž. sazbou daně - Základ                  |
| 2452                         | ř.245 - se sníž. sazbou daně - Daň                     |
| 2501                         | ř.250 - od osob reg. v jiném čl.státě - Základ          |
| 2502                         | ř.250 - od osob reg. v jiném čl.státě - Daň             |
| 2551                         | ř.255 - od osob nereg. v jiném čl.státě - Základ        |
| 2552                         | ř.255 - od osob nereg. v jiném čl.státě - Daň           |
| 2601                         | ř.260 - se zákl. sazbou daně – Základ                   |
| 2602                         | ř.260 - se zákl. sazbou daně – Daň                      |
| 2651                         | ř.265 - se sníž. sazbou daně – Základ                   |
| 2652                         | ř.265 - se sníž. sazbou daně - Daň                      |
| 2701                         | ř.270 - se zákl. sazbou daně - Základ                  |
| 2702                         | ř.270 - se zákl. sazbou daně - Daň                     |
| 2751                         | ř.275 - se sníž. sazbou daně - Základ                  |
| 2752                         | ř.275 - se sníž. sazbou daně - Daň                     |
| 3101                         | ř.310 - se zákl. sazbou daně - Základ                   |
| 3102                         | ř.310 - se zákl. sazbou daně - Daň, plný nárok          |
| 3103                         | ř.310 - se zákl. sazbou daně - Daň, krác. nárok         |
| 3151                         | ř.315 - se sníž. sazbou daně - Základ                   |
| 3152                         | ř.315 - se sníž. sazbou daně - Daň, plný nárok          |
| 3153                         | ř.315 - se sníž. sazbou daně - Daň, krác. nárok         |
| 3201                         | ř.320 - se zákl. sazbou daně - Základ                  |
| 3202                         | ř.320 - se zákl. sazbou daně - Daň, plný nárok         |
| 3203                         | ř.320 - se zákl. sazbou daně - Daň, krác. nárok        |
| 3251                         | ř.325 - se sníž. sazbou daně - Základ                  |
| 3252                         | ř.325 - se sníž. sazbou daně - Daň, plný nárok         |
| 3253                         | ř.325 - se sníž. sazbou daně - Daň, krác. nárok        |
| 3301                         | ř.330 - se zákl. sazbou daně - Základ                   |
| 3302                         | ř.330 - se zákl. sazbou daně - Daň, plný nárok          |
| 3303                         | ř.330 - se zákl. sazbou daně - Daň, krác. nárok         |
| 3351                         | ř.335 - se sníž. sazbou daně - Základ                  |
| 3352                         | ř.335 - se sníž. sazbou daně - Daň, plný nárok         |
| 3353                         | ř.335 - se sníž. sazbou daně - Daň, krác. nárok        |
| 3401                         | ř.340 - se zákl. sazbou daně - Základ                   |
| 3402                         | ř.340 - se zákl. sazbou daně - Daň, plný nárok          |
| 3403                         | ř.340 - se zákl. sazbou daně - Daň, krác. nárok         |
| 3451                         | ř.345 - se sníž. sazbou daně - Základ                  |
| 3452                         | ř.345 - se sníž. sazbou daně - Daň, plný nárok         |
| 3453                         | ř.345 - se sníž. sazbou daně - Daň, krác. nárok        |
| 3501                         | ř.350 - se zákl. sazbou daně - Základ                  |
| 3502                         | ř.350 - se zákl. sazbou daně - Daň, plný nárok         |
| 3503                         | ř.350 - se zákl. sazbou daně - Daň, krác. nárok        |
| 3551                         | ř.355 - se sníž. sazbou daně - Základ                  |
| 3552                         | ř.355 - se sníž. sazbou daně - Daň, plný nárok         |
| 3553                         | ř.355 - se sníž. sazbou daně - Daň, krác. nárok        |
| 3601                         | ř.360 - od osob reg. v jiném čl.státě - Základ          |
| 3602                         | ř.360 - od osob reg. v jiném čl.státě - Daň             |
| 3603                         | ř.360 - od osob reg. v jiném čl.státě - Daň, krác.      |
| 3651                         | ř.365 - od osob nereg. v jiném čl.státě - Základ        |
| 3652                         | ř.365 - od osob nereg. v jiném čl.státě - Daň           |
| 3653                         | ř.365 - od osob nereg. v jiném čl.státě - Daň, kr.      |
| 3702                         | ř.370 - při změně režimu - Daň, plný nárok             |
| 3703                         | ř.370 - při změně režimu - Daň, krác. nárok            |
| 3803                         | ř.380 - celková suma pro krácení nároku na odpočet daně |
| 3902                         | ř.390 - celková suma plného nároku na odpočet daně      |
| 4102                         | ř.410 - dodání zboží do jiného čl.státu                 |
| 4202                         | ř.420 - dodání nového dopr.prostř. osobě reg.           |
| 4252                         | ř.425 - dodání nového dopr. prostř. osobě nereg.        |
| 4302                         | ř.430 - vývoz zboží (§66)                               |
| 4402                         | ř.440 - Ost.plnění osv.od daně s nárok. na odpočet      |
| 5102                         | ř.510 - Celk. usk.plnění s nárokem na odpočet daně      |
| 5202                         | ř.520 - Uskut. plnění, která se nezapoč. do koef.       |
| 5302                         | ř.530 - Celk. osv.usk.plnění bez nároku na odpočet      |
| 5402                         | ř.540 - Usk.plnění nezapoč. do výpočtu koeficientu      |
| 5503                         | ř.550 - Vypočt. poměr.část odp.daně (§76) - Koef.       |
| 5502                         | ř.550 - Vypočt. poměr.část odp.daně (§76)               |
| 5603                         | ř.560 - Vypoř. odp. daně (§76 odst.7-10) - Koef.        |
| 5602                         | ř.560 - Vypoř. odp. daně (§76 odst.7-10)                |
| 5702                         | ř.570 - Úprava odpočtu daně (§78)                       |
| 5802                         | ř.580 - Vyrovnání odpočtu daně (§79)                    |
| 6002                         | ř.600 - Vrácení daně                                    |
| 7102                         | ř.710 - Vypořádání daně na výstupu (§91)                |
| 7302                         | ř.730 - Daň na výstupu                                  |
| 7502                         | ř.750 - Odpočet daně                                    |
| 7532                         | ř.753 - Vlastní daňová povinnost                        |
| 7542                         | ř.754 - Nadměrný odpočet                                |
| 7802                         | ř.780 - Změna daň.povinnosti při podání dod. přiz.      |
| 8101                         | ř.810 - Pořízení zboží prostřední osobou                |
| 8151                         | ř.815 - Dodání zboží prostřední osobou                  |

## <a name="configure-the-er-model-and-format-for-the-report"></a>Konfigurace modelu ER a formátu výkazu
Ke kontrole nebo změně konfigurace výkazu DPH můžete použít pracovní prostor **Elektronické podání**. Přejděte na stránku **Konfigurace** a v seznamu modelů vyberte **Model prohlášení DPH**. Tento model je společný pro Rakousko, Českou republiku, Estonsko, Finsko, Lotyšsko a Litvu a agreguje daňové údaje potřebné pro přiznání DPH. Chcete-li zkontrolovat nebo změnit formát výkazu DPH pro uživatele ve funkci právnických osob v České republice, vyberte **Přiznání k DPH (CZ)**, což je podřízená položka **modelu prohlášení DPH** ve stromu modelu. Vyberte ji a klikněte na **Návrhář** v podokně akcí k zobrazení nebo změně formátu. Další informace získáte v tématu [Elektronické vykazování.](../../dev-itpro/analytics/general-electronic-reporting.md)

## <a name="generate-the-vat-statement"></a>Generování výkazu DPH
Pokud chcete generovat soubor DPH XML, otevřete stránku **Platby DPH**, vyberte doklady a klikněte na **Export DPH do souboru XML**.



