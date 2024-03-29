---
title: Konfigurace účetních struktur
description: Tento článek obsahuje informace o účetní struktuře a finančních dimenzích.
author: aprilolson
ms.date: 10/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3fbdd6e2cac61c358848a21e1126bea900e86b2
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713924"
---
# <a name="configure-account-structures"></a>Konfigurovat účetní struktury

[!include[banner](../includes/banner.md)]

Účetní struktury používají hlavní účet a finanční dimenze k vytváření sady pravidel, která určuje pořadí a hodnoty používané při zadávání čísla účtu. Můžete nastavit tolik účetních struktur, kolik vaše firma potřebuje. Účetní struktury jsou přiřazeny nastavení hlavní knihy společnosti, aby bylo možné je sdílet.

Při vytváření účetní struktury je maximální počet segmentů 11. Pokud potřebujete více než 11 segmentů, důkladně posuďte nastavení a požadavky, protože budou mít vliv na zkušenosti uživatele. Zvažte, zda některý segment může být odvozen ve scénáři výkaznictví pomocí hierarchie namísto při zadávání dat, nebo pomocí uživatelem definovaných polí. Například pokud chcete vykazovat ve skladovém místě, ale může vypočítat umístění podle oddělení nebo nákladového střediska, nepotřebujete umístění jako finanční dimenzi. Pokud po vyhodnocení určíte, zda je potřeba více než 11 segmentů, můžete přidat další segmenty pomocí rozšířeného pravidla.

Účetní struktury vyžadují hlavní účet. Hlavní účet nemusí být první segment ve struktuře, ale určuje, která účetní struktura se používá při zadání čísla účtu. Z tohoto důvodu může hodnota hlavního účtu existovat pouze v jedné struktuře přiřazené do hlavní knihy tak, aby se nepřekrývaly. Poté, co je identifikována účetní struktura, seznam povolených hodnot je filtrován tak, aby prováděly uživatele výběrem pouze platných hodnot dimenze, což snižuje možnost nesprávné položky deníku.

> [!NOTE] 
> Pokud plánujete vytvářet rozpočet na základě finanční dimenze, bude muset být součástí účetní struktury. Rozpočtování aktuálně nevyužívá rozšířená pravidla.

## <a name="example"></a>Příklad
Pro ilustraci vhodného nastavení účetní struktury předpokládejme, že chce společnost sledovat svůj rozvahový účet (100000..399999) na úrovni účtu a finanční dimenze obchodní jednotky. Pro účty příjmů a výdajů (400000..999999) sledují finanční dimenze, organizační jednotku, oddělení a nákladové středisko. Pokud uskutečňují prodeje, chtějí také sledovat odběratele. Pomocí tohoto scénáře je doporučeno používat dvě účetní struktury, které jsou přiřazeny k hlavní knize společnosti – jednu pro účet rozvahy a druhou pro účty zisků a ztrát. Aby bylo možné optimalizovat zkušenosti a ověření uživatele, zákazník by měl používat pokročilé pravidlo, které se používá pouze v případě, že se používá také prodejní účet.

**Struktura rozvahového účtu**

|Hlavní účet          | Obchodní jednotka    |
|----------------------|-----------|
|100000..399999 | *;"&nbsp;"|

**Struktura účtu zisků a ztrát**

|Hlavní účet          | Obchodní jednotka    |Oddělení          | Nákladové středisko    | &nbsp; |
|----------------------|------------------|--------------------|-----------|---|
|400000..999999 | \*;"&nbsp;"| \*;"&nbsp;"| \*;"&nbsp;"| \*;"&nbsp;"|

**Rozšířené pravidlo pro přidání zákazníka**

Kritéria: Tam, kde je hlavní účet mezi 400000 a 499999, přidejte odběratele. Nemůže zůstat prázdné.

|Zákazník         |
|-----------------|
|\* |

V tomto zjednodušeném příkladu jsou všechny hodnoty a prázdné hodnoty povoleny, takže se používá \* a „&nbsp;“.

## <a name="segments-and-allowed-values"></a>Segmenty a povolené hodnoty
Oddíl **Segmenty** a **povolené hodnoty podrobnosti** obsahuje mřížku jako zkušenost pro zadávání pravidel, která bude následovat při ověření během zaúčtování. Můžete psát přímo do buněk v mřížce, importovat je z aplikace Excel nebo použít oddíl **podrobnosti povolené hodnoty**, která vás provede.

Oddíl **podrobnosti povolené hodnoty** vás provede kritérii vytváření pomocí **operátorů**, například začíná na, je mezi, zahrnuje a mnoha dalšími.

[![Povolit hodnoty.](./media/account.png)](./media/account.png) 

Pokud neexistují další možné hodnoty pro výběr v souladu s nastavením účetní struktury, budou povolené hodnoty se nastaví na výchozí na stránce zadání deníku nebo rozúčtování.

Zde je příklad možnosti **Struktura účtu zisků a ztrát**.

|Hlavní účet          | Obchodní jednotka    |Oddělení          | Nákladové středisko    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Při zadávání deníku a výběru účtu v rozsahu zisků a ztrát způsobí výběr obchodní jednotky 002, že hodnoty 022 a 014 budou výchozí na ovládacím prvku účtu. K tomuto chování dojde také u stránky rozúčtování. 

## <a name="more-than-seven-criteria-needed"></a>Je potřeba více než sedm kritérií

Pokud máte více než sedm kritérií, která jsou potřeba, můžete pokračovat v jejich přidávání na dalším řádku. Při práci v oddílu **Podrobnosti povolené hodnoty** si všimnete, že už není dostupná možnost **+ Přidat nové** kritérium pro zadání sedmého kritéria. Je to způsobeno mnoha faktory jako: 
 - Šířka sloupce 
 - Způsob uložení dat 
 - Výkon ovládacího prvku **povolená hodnota podrobnosti**
 - Použitelnost  

> [!NOTE]
> Upgrade z Microsoft Dynamics AX 2012, kde je specifikováno více než sedm kritérií, není podporováno. Před dokončením upgradu na finanční a provozní aplikace je nutné jej opravit. 

Chcete-li přidat další kritéria, klepněte na tlačítko **duplicitní v segmentu** a **Oddíl Povolené hodnoty**. Tím se kritéria zkopírují na nový řádek. Potom můžete přepsat nebo změnit oddíl **Podrobnosti povolené hodnoty**.

## <a name="best-practices"></a>Doporučené postupy
Při nastavování účetních struktur existují doporučené postupy, které můžete následovat. Jde však pouze o pokyny, takže by měla být v rámci takové diskuse zvážena holistická diskuse o vaší firmě, plánu rozvoje a údržbě.

- Hlavní účet vytvořte jako první nebo co nejbližší účetní struktuře, aby uživatelé měli při vytváření účtu co nejlepší možnosti vedení.
  
  - Ověřte, že všechna řešení třetích stran, která hodláte používat, podporují hlavní účet na první pozici.

- Znovu použijte účetní struktury co nejvíce je možné, aby se snížila údržba mezi právnickými osobami.

- Pro odchylky mezi právnickými osobami zvažte použití rozšířených pravidla tak, aby bylo možné opakovaně použít účetní struktury.

- Při definování povolených hodnot co nejvíce používejte rozsahy a zástupné znaky. To nejen umožňuje rozvíjet a měnit bez údržby, ale systém funguje ideálněji při této konfiguraci.

- Nestačí napsat hvězdičku pro každý segment účetní struktury a spoléhat na pokročilá pravidla. To může být obtížné pro správu a často vede k chybám uživatelů během údržby, což může způsobit neschopnost systému účtovat.

## <a name="account-structure-activation"></a>Aktivace účetní struktury
Jakmile jste s novým nastavením nebo změnou účetní struktury spokojeni, musíte je aktivovat. Pokud je účetní struktura přiřazena hlavní knize, může být tato aktivace zdlouhavý proces, protože všechny nezaúčtované transakce v systému musí být synchronizované podle nové struktury. Zaúčtované transakce nejsou změnami účetní struktury ovlivněny. Od verze aplikace 10.0.31 nová funkce s názvem **Zlepšení výkonu aktivace struktury účtu** je k dispozici ve správě funkcí. Další informace o této nové funkci aktivace struktury účtu naleznete v části [Zlepšení výkonu aktivace struktury účtu](account-structure-improvement.md). 

Další informace naleznete v tématu [Plánování účtových osnov](plan-chart-of-accounts.md), [finanční dimenze](financial-dimensions.md) a [Zadání kombinací účtů a dimenzí (segmentovaná kontrola položek)](enter-account-dimension-combinations-segmented-entry-control.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
