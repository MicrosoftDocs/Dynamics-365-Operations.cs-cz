---
title: Fiskální kalendář, fiskální roky a období
description: Tento článek popisuje fiskální kalendáře, fiskální roky a období a způsoby jejich využití pro právnické osoby, dlouhodobý majetek a tvorbu rozpočtu.
author: aprilolson
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1583df4650d0b36ecc2cb0d3e2d3a410aa807ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909091"
---
# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Fiskální kalendář, fiskální roky a období

[!include [banner](../includes/banner.md)]

Tento článek popisuje fiskální kalendáře, fiskální roky a období a způsoby jejich využití pro právnické osoby, dlouhodobý majetek a tvorbu rozpočtu.

Fiskální kalendáře poskytují systém pro finanční aktivity organizace. Každý fiskální kalendář obsahuje jeden nebo více fiskálních roků a každý fiskální rok obsahuje více období. Fiskální kalendáře mohou být založeny na kalendářním roce od 1. ledna po 31. prosince nebo libovolných datech, která vyberete. V některých organizacích vyberte například fiskálního kalendář, které začíná datem 1. července jednoho roku a končí 30. června následujícího roku. 

Počet fiskálních kalendářů, které můžete vytvořit, není nijak omezen a není omezen ani počet fiskálních roků, které lze vytvořit pro fiskální kalendář. Každý fiskální kalendář je nezávislý na organizaci a lze ho použít více právnickými osobami v rámci organizace. Například organizace má osm oddělení a každé oddělení je samostatná právnická osoba. Pět z nich sdílí stejný fiskální kalendář a tři používají různé fiskální kalendáře. Můžete vytvořit jeden fiskální kalendář pro pět právnických osob, které sdílejí stejný fiskální kalendář, a vytvořit samostatné fiskální kalendáře pro ostatní právnické osoby.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Vytváření fiskálních kalendářů, fiskálních roků a období
Na stránce Fiskální kalendáře můžete vytvářet a odstraňovat fiskální kalendáře, fiskální roky a období. Lze rovněž rozdělit existující období a vytvořit období uzávěrky, které lze použít k uzavření fiskálního roku. 

Období uzávěrky slouží k oddělení transakcí v hlavní knize, které jsou vytvořeny po ukončení fiskálního roku. Pokud jsou uzávěrkové transakce v jednom fiskálním období, je snazší vytvořit finanční výkazy, které zahrnují nebo vylučují uzávěrkové položky různých typů. Pokud je fiskální rok rozdělen na 12 fiskálních období, období uzávěrky je obvykle 13. období. Lze však vytvořit období uzávěrky z libovolného období se stavem Otevřené. 

Při vytváření období uzávěrky vyberte období, které má stav Otevřené a které obsahuje data, která chcete použít. Nové období uzávěrky zkopíruje počáteční a koncová data z existujícího období. Původní období bude nadále existovat. Vyberte například Období 12, což je poslední období fiskálního roku s daty od 1. do 31. srpna. Zadejte název období uzávěrky, jako např. Uzavření. Po vytvoření nového období uzávěrky nyní máte původní období a období uzávěrky. Obě mají data zahájení 1. srpna a končí 31. srpna.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Výběr fiskálních kalendářů pro hlavní knihy, dlouhodobý majetek a rozpočtové cykly
Fiskální kalendáře se používají pro odpis dlouhodobého majetku finanční transakce a rozpočtové cykly. Když vytváříte fiskální kalendář můžete ho použít pro několik účelů. Můžete vybrat fiskální kalendář pro knihu dlouhodobého majetku, a udělat z něj kalendář dlouhodobého majetku. Můžete vybrat fiskální kalendář pro hlavní knihu a udělat z něj kalendář hlavní knihy. A můžete vybrat fiskální kalendář pro rozpočtový cyklus a udělat z něj kalendář rozpočtu. Pro všechny tyto možnosti můžete používat stejný fiskální kalendář.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Výběr fiskálního kalendáře pro právnickou osobu

Vyberte fiskální kalendář, který chcete používat pro hlavní knihu pro vaši právnickou osobu ve formuláři Hlavní kniha. Fiskální kalendář musí být na stránce Hlavní kniha vybrán pro každou právnickou osobu. Po výběru fiskálního kalendáře můžete na stránce Kalendář hlavní knihy nastavit stavy období a oprávnění pro všechna období, která jsou součástí fiskálního roku.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Výběr fiskálního kalendáře pro dlouhodobý majetek

Můžete vybrat fiskální kalendář pro knihu dlouhodobého majetku a tento fiskální kalendář se bude používat pro dlouhodobý majetek, který používá vybranou knihu. Můžete vybírat ze všech fiskálních kalendářů definovaných na stránce Fiskální kalendáře.

### <a name="define-budget-cycle-time-spans"></a>Definice délky rozpočtového cyklu

Rozpočtové cykly je doba, během které se rozpočet používá. Rozpočtové cykly může zahrnovat část fiskálního roku nebo více fiskálních roků, jako je například dvouletý rozpočtový cyklus nebo tříletý rozpočtový cyklus. Délka rozpočtového cyklu určuje počet období, které jsou součástí rozpočtového cyklu. K určení délky rozpočtového cyklu použijte stránku Délka rozpočtových cyklů.

## <a name="maintain-periods-for-your-organization"></a>Udržovací období pro organizaci
K zobrazení podrobností fiskálního kalendáře, fiskálních roků a období, které používá vaše organizace, můžete použít stránku Kalendář hlavní knihy. Můžete také změnit stav období a vybrat uživatele, kteří mohou účtovat účetní transakce do období. Například na začátku nového období můžete chtít, aby jedna skupina uživatelů dokončila zaúčtování finančních transakcí z předchozího období, zatímco jiná skupina bude pracovat pouze v novém období.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
