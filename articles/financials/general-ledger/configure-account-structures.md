---
title: "Konfigurovat účetní struktury"
description: "Toto téma obsahuje informace o účetní struktuře a finančních dimenzích."
author: aprilolson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8435389a523d8393e9d4daa0cb1244203c0dbb12
ms.openlocfilehash: a0665f5aec2a0809ecb383c1d4adf4c2072c9569
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="configure-account-structures"></a>Konfigurovat účetní struktury

[!include[banner](../includes/banner.md)]

Účetní struktury používají hlavní účet a finanční dimenze k vytváření sady pravidel, která určuje pořadí a hodnoty používané při zadávání čísla účtu. Můžete nastavit tolik účetních struktur, kolik vaše firma potřebuje. Účetní struktury jsou přiřazeny nastavení hlavní knihy společnosti, aby bylo možné je sdílet.

Při vytváření účetní struktury je maximální počet segmentů 11. Pokud potřebujete další segmenty než tento, důkladně posuďte nastavení a požadavky, protože budou mít vliv na zkušenosti uživatele. Zvažte, zda některý segment může být odvozen ve scénáři výkaznictví pomocí hierarchie namísto při zadávání dat, nebo pomocí uživatelem definovaných polí. Například pokud chcete vykazovat ve skladovém místě, ale může vypočítat umístění podle oddělení nebo nákladového střediska, nepotřebujete umístění jako finanční dimenzi. Pokud po vyhodnocení určíte, zda je potřeba více než 11 segmentů, můžete přidat další segmenty pomocí rozšířeného pravidla.

Účetní struktury vyžadují hlavní účet. Hlavní účet nemusí být první segment ve struktuře, ale určuje, která účetní struktura se používá při zadání čísla účtu. Z tohoto důvodu může hodnota hlavního účtu existovat pouze v jedné struktuře přiřazené do hlavní knihy tak, aby se nepřekrývaly. Poté, co je identifikována účetní struktura, seznam povolených hodnot je filtrován tak, aby prováděly uživatele výběrem pouze platných hodnot dimenze, což snižuje možnost nesprávné položky deníku.

> [!NOTE] 
> Pokud plánujete vytvářet rozpočet na základě finanční dimenze, bude muset být součástí účetní struktury. Rozpočtování aktuálně nevyužívá rozšířená pravidla.

## <a name="example"></a>Příklad
Pro ilustraci vhodného nastavení účetní struktury předpokládejme, že chce společnost sledovat svůj rozvahový účet (100000..399999) na úrovni účtu a finanční dimenze obchodní jednotky. Pro účty příjmů a výdajů (400000..999999) sledují finanční dimenze, organizační jednotku, oddělení a nákladové středisko. Pokud uskutečňují prodeje, chtějí také sledovat odběratele. Pomocí tohoto scénáře je doporučeno používat dvě účetní struktury, které jsou přiřazeny k hlavní knize společnosti – jednu pro účet rozvahy a druhou pro účty zisků a ztrát. Aby bylo možné optimalizovat zkušenosti a ověření uživatele, zákazník by měl používat pokročilé pravidlo, které se používá pouze v případě, že se používá také prodejní účet.

**Struktura rozvahového účtu**

|Hlavní účet          | Obchodní jednotka    |
|----------------------|-----------|
|100000..399999 | *;” “|

**Struktura účtu zisků a ztrát**

|Hlavní účet          | Obchodní jednotka    |Oddělení          | Nákladové středisko    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | *;” “|*;” “|*;” “|*;” “|

**Rozšířené pravidlo pro přidání zákazníka**

Kritéria: Tam, kde je hlavní účet mezi 400000 a 499999, přidejte odběratele. Nemůže zůstat prázdná.

|Zákazník         |
|-----------------|
|* |

V tomto zjednodušeném příkladu jsou všechny hodnoty a prázdné hodnoty povoleny, takže se používá * a “ “.

## <a name="segments-and-allowed-values"></a>Segmenty a povolené hodnoty
Oddíl **Segmenty** a **povolené hodnoty podrobnosti** obsahuje mřížku jako zkušenost pro zadávání pravidel, která bude následovat při ověření během zaúčtování. Můžete psát přímo do buněk v mřížce, importovat je z aplikace Excel nebo použít oddíl **podrobnosti povolené hodnoty**, která vás provede.

Oddíl **podrobnosti povolené hodnoty** vás provede kritérii vytváření pomocí **operátorů**, například začíná na, je mezi, zahrnuje a mnoha dalšími.

[![Povolit hodnoty](./media/account.png)](./media/account.png) 

## <a name="more-than-7-criteria-needed"></a>Je potřeba více než 7 kritérií.

Pokud máte více než 7 kritérií, která jsou potřeba, můžete pokračovat v jejich přidávání na dalším řádku. Při práci v oddílu **podrobnosti povolené hodnoty** si všimnete, že kritérium **+ přidat nový** již není aktivní pro zadání sedmého kritéria. Je to způsobeno mnoha faktory jako: 
 - Šířka sloupce 
 - Způsob uložení dat 
 - Výkon ovládacího prvku **povolená hodnota podrobnosti**
 - Použitelnost  
 
Chcete-li přidat další kritéria, klepněte na tlačítko **duplicitní v segmentu** a **Oddíl Povolené hodnoty**. Tím se kritéria zkopírují na nový řádek. Potom můžete přepsat nebo změnit oddíl **Podrobnosti povolené hodnoty**.

(ODKAZ NA VIDEOZÁZNAM, KTERÝ BUDE VYTVOŘEN)

## <a name="best-practices"></a>Doporučené postupy
Při nastavování účetních struktur existují doporučené postupy, které můžete následovat. Jde však pouze o pokyny, takže by měla být v rámci takové diskuse zvážena holistická diskuse o vaší firmě, plánu rozvoje a údržbě.

- Hlavní účet vytvořte jako první nebo co nejbližší účetní struktuře, aby uživatelé měli při vytváření účtu co nejlepší možnosti vedení.

- Znovu použijte účetní struktury co nejvíce je možné, aby se snížila údržba mezi právnickými osobami.

- Pro odchylky mezi právnickými osobami zvažte použití rozšířených pravidla tak, aby bylo možné opakovaně použít účetní struktury.

- Při definování povolených hodnot co nejvíce používejte rozsahy a zástupné znaky. To nejen umožňuje rozvíjet a měnit bez údržby, ale systém funguje ideálněji při této konfiguraci.

- Nestačí napsat hvězdičku pro každý segment účetní struktury a spoléhat na pokročilá pravidla. To může být obtížné pro správu a často vede k chybám uživatelů během údržby, což může způsobit neschopnost systému účtovat.

## <a name="account-structure-activation"></a>Aktivace účetní struktury
Jakmile jste s novým nastavením nebo změnou účetní struktury spokojení, musíte ji aktivovat. Pokud je účetní struktura přiřazena hlavní knize, může být tato aktivace zdlouhavý proces, protože všechny nezaúčtované transakce v systému musí být synchronizované podle nové struktury. Zaúčtované transakce nejsou změnami účetní struktury ovlivněny.

Další informace naleznete v tématu [Plánování účtových osnov](plan-chart-of-accounts.md), [finanční dimenze](financial-dimensions.md) a [Zadání kombinací účtů a dimenzí (segmentovaná kontrola položek)](enter-account-dimension-combinations-segmented-entry-control.md).

