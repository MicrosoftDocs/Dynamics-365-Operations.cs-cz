---
title: "Ohlášení dokončení kusovníku"
description: "Tento článek obsahuje informace o ohlášení kusovníků jako dokončených."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMReportFinish, BOMReportFinishMax
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 26b5029068904d4af5849eab9135f50b3291f642
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="report-boms-as-finished"></a>Ohlášení dokončení kusovníku

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o ohlášení kusovníků jako dokončených.

Stránky **Vykázat jako dokončené** a **Maximální dokončená výroba** složí k vykázání kusovníků v dokončeném stavu. Proces vykázání dokončeného kusovníku je koncepčně stejný jako proces vykázání dokončené výrobní zakázky. Tento proces lze použít například v jednoduchých procesech sestavení a kompletace, u kterých nejsou potřeba rozšířené možnosti výrobních zakázek. Na stránce **Vykázat jako dokončené** můžete vykázat více dokončených kusovníků najednou. Na stránce **Maximální dokončená výroba** můžete vykázat pouze jeden kusovník jako dokončený. Stránka **Hlášení jako dokončené** je k dispozici z položky nabídky v modulu Řízení zásob a obě stránky jsou k dispozici jako položky nabídky na stránce **Uvolněné produkty**.

## <a name="report-as-finished-page"></a>Stránka Vykázat jako dokončené
Po otevření stránky **Vykázat jako dokončené** z uvolněného produktu systém navrhne, abyste jako dokončené vykázali výchozí množství standardních zásob. Ve výchozím nastavení se zobrazuje aktivní verze kusovníku, avšak máte možnost změny na jinou schválenou verzi kusovníku. Na stránce může také odstraňovat záznamy a vytvářet nové záznamy pro uvolněné produkty, které mají být vykázány jako dokončené. Chcete-li produkty vybrat pomocí dotazu, klikněte na položku nabídky **Vybrat**. Pro vybrané produkty kliknutím na tlačítko **OK** ručně potvrďte výkaz jako dokončený. Proces lze rovněž nastavit ke spuštění v dávce. Jakmile je vykázání dokončení procesu potvrzeno, systém vytvoří deník kusovníku, ve kterém je zpracováno zaúčtování zásob. Tento deník obsahuje jednu řádkovou položku pro dokončený produkt a řádkovou položku pro každý řádek kusovníku. Můžete určit, zda je deník zaúčtovat automaticky, nebo zda zůstane otevřený pro další úpravy.

## <a name="max-report-as-finished-page"></a>Maximum Stránka Hlásit jako dokončené
Na stránce **Maximální dokončená výroba** určuje každý řádek kusovníku počet kusů produktu, které mohou být vykázány jako dokončené. Tento výpočet vychází z fyzicky dostupných zásob na skladě pro každý řádek kusovníku. V následujícím příkladu spotřebovává jeden kus čísla položky PZ dva kusy suroviny SU10 a jeden kus suroviny SU20. Vzhledem k tomu, že na skladě je pouze 10 kusů suroviny SU10, lze jako dokončené vykázat maximálně 5 kusů PZ. Tato hodnota se zobrazuje v poli **Maximální dokončená výroba**.

| Úroveň | Číslo zboží | Množství | Na skladě | Maximum Hlášení jako dokončené |
|-------|-------------|----------|---------|-------------------------|
| 0     | PZ          |  1       | 0       | 5                       |
| 1     | SU10        | -2       | 10      | 5                       |
| 1     | SU20        | -1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>Kusovníky s více úrovněmi
Pokud má kusovník více úrovní, můžete pomocí pole **Rozbalení** určit způsob, jakým jsou materiály zaúčtovány na všech úrovních. Toto pole je k dispozici na stránce **Vykázat jako dokončené** i na stránce **Maximální dokončená výroba**. Existují tyto možnosti:

-   **Nikdy** – Podúrovně kusovníku se v případě nedostatku materiálu nerozbalí.
-   **Vždy** – Zcela se rozbalí všechny podúrovně kusovníku. Žádné dostupné zásoby na skladě nebudou použity pro položky polotovarů komponent.
-   **Pří nedostatku** – Podúrovně kusovníku se rozbalí pouze tehdy, není-li potřebné množství materiálu plně k dispozici.

### <a name="example"></a>Příklad

V tomto příkladu jsou tři kusy hotového produktu (číslo položky PZ) připraveny k vykázání jako dokončené. Kusovník je dvojúrovňový (jak je znázorněno).

| Úroveň | Číslo zboží | Množství na řádku kusovníku | Na skladě |
|-------|-------------|-------------------|---------|
| 0     | PZ          |                   |         |
| 1     | PC        | 1                 | 2       |
| 1     | SU          | 1                 |         |

V následujících tabulkách je znázorněn způsob, jakým má nastavení v poli **Rozbalení** vliv na způsob generování řádků deníku kusovníku. **Rozbalení: Nikdy**

| Úroveň | Číslo zboží | Množství |
|-------|-------------|----------|
| 0     | PZ          | 3        |
| 1     | PC        | -3       |

Jak ukazuje předchozí tabulka, pouze číslo položky COMP je považováno za odečtené v deníku. Číslo zboží RM, které je součástí modulu COMP, není rozepsáno do řádku deníku a dvě kusy COMP na skladě nejsou zahrnuty. **Rozbalení: Vždy**

| Úroveň | Číslo zboží | Množství |
|-------|-------------|----------|
| 0     | PZ          | 3        |
| 1     | SU          | -3       |

V tomto případě je číslo položky PC rozbaleno na úroveň surovin, číslo položky SU. Dva kusy PC na skladě nejsou zohledněny v množství SU ke spotřebování. **Rozbalení: Při nedostatku**

| Úroveň | Číslo zboží | Množství |
|-------|-------------|----------|
| 0     | PZ          | 3        |
| 1     | PC        | -2       |
| 1     | SU          | -1       |

V tomto případě jsou dva kusy PC na skladě zohledněny. Nicméně vzhledem k tomu, že jsou potřeba tři kusy čísla položky PZ, je k vyrobení dalšího kusu PC potřeba také jeden kus čísla položky SU.




