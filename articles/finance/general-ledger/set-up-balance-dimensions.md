---
title: Jak nastavím vyrovnávací finanční dimenze?
description: Toto téma popisuje možnosti nastavení a používání funkce Vyrovnávání finanční dimenze.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: 188c15c4cb0c295a9fcbb08273ddb391fbc29e24
ms.sourcegitcommit: b4c78655f2ab4b0e7ead96dfb9cf087a18014253
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2021
ms.locfileid: "7468933"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Jak nastavím vyrovnávací finanční dimenze?

[!include [banner](../includes/banner.md)]

Toto téma popisuje možnosti nastavení a používání funkce Vyrovnávání finanční dimenze.

## <a name="symptom"></a>Příznak

Existují dvě možnosti nastavení vyrovnávání finančních dimenzí. První možností je použít pole **Vyrovnávání finanční dimenze** na stránce nastavení **hlavní kniha** (**Hlavní kniha \> Nastavení hlavní knihy \> hlavní kniha**). Druhou možností je použití pole **Požadovat vyrovnání dimenzí** na stránce **Finanční dimenze** (**Hlavní kniha > Účetní osnova \> Dimenze \> Finanční dimenze**). Toto téma vysvětluje rozdíl mezi těmito dvěma možnostmi.

## <a name="resolution"></a>Řešení

Organizace obvykle používají vyrovnávací dimenze ke generování rozvahy, která je v rovnováze na úrovni finanční dimenze. Povolením kterékoli z těchto funkcí se nevyrovnané dimenze neuvedou do rovnováhy. Před povolením obou funkcí musíte nejprve ručně upravit položky, abyste uvedli rozvahu do rovnováhy.

Tyto dvě možnosti se vzájemně vylučují. Možnost, kterou vaše organizace používá, by měla vycházet z vašich obchodních požadavků. Často slýcháme o zákaznících, kteří definují dimenzi vyrovnávání jak v nastavení hlavní knihy, tak v nastavení finanční dimenze, a poté dokončí některé nebo všechna další potřebná nastavení. Stále však nemohou zveřejňovat příspěvky kvůli nerovnováze na úrovni finanční dimenze.

Následující části popisují dvě možnosti a vysvětlují, jak je nastavit.

### <a name="ledger--balancing-financial-dimension"></a>Hlavní kniha - vyrovnávací finanční dimenze

Vyvažovací rozměr na stránce nastavení **hlavní kniha** slouží k povolení mezijednotkového účetnictví. Funkci zapněte pomocí těchto kroků:

1. Určete, která finanční dimenze bude dimenzí vyrovnávací.

    - Tato funkce vám umožňuje vybrat jako vyrovnávací dimenzi pouze jednu finanční dimenzi.
    - Zatím nevybírejte dimenzi na stránce nastavení **hlavní knihy**.
    - Ujistěte se, že je vaše rozvaha pro vybranou finanční dimenzi již vyvážená.

2. Aktualizujte účetní strukturu pro finanční dimenzi vyrovnávání.

    - Je nutné zahrnout finanční dimenzi, která je součástí všech struktur účtu, které jsou přiřazeny k hlavní knize.
    - Finanční dimenze nesmí ve struktuře účtu povolovat mezery. Toto omezení zajišťuje, že každý účetní záznam, který je zaúčtován do hlavní knihy, obsahuje hodnotu finanční dimenze. Při použití vyrovnávacích dimenzí není prázdná dimenze platná.

3. Na stránce **Účty pro automatické transakce** (**Hlavní kniha \> Nastavení zaúčtování \> Účty pro automatické transakce**) definujte mezijednotkové debetní a kreditní hlavní účty.
4. Na stránce nastavení **Hlavní kniha** (**Hlavní kniha \> Nastavení hlavní knihy \> Hlavní kniha**) v poli **Vyrovnávací finanční dimenze** vyberte finanční dimenzi pro použití ve vyrovnávání.

Pokud vybraná finanční dimenze není při zadávání a zaúčtování transakcí vyvážená, systém automaticky přidá debetní nebo kreditní položky, které jsou nutné k vyrovnání účetního záznamu během účtování. Debetní a kreditní účty hlavní knihy pro transakci mezi jednotkami jsou uvedeny na zaúčtovaném dokladu v hlavní knize. Nebudou však zobrazeny v denících nebo zdrojových dokumentech, pro které byly zaúčtovány účetní položky.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Finanční dimenze - Požaduje vyvážení dimenze

Ačkoli vyrovnávací dimenze na stránce **Finanční dimenze** obvykle používají společnosti veřejného sektoru, funkce není propojena s žádným konfiguračním klíčem veřejného sektoru. Protože v systému není žádné omezení, můžete tuto funkci používat, i když vaše organizace není subjektem veřejného sektoru.

Tato funkce se obvykle používá v zákaznické základně veřejného sektoru, protože vyžaduje, aby se definice účtování používaly k automatickému vyrovnání každé transakce. Nepoužívá mezijednotkové debetní a kreditní účty, které jsou definovány na stránce **Účty pro automatické transakce** pro automatické vyrovnání účetních záznamů. Pokud není účetní záznam po použití definic účtování vyvážen na úrovni dimenze, transakce nebude zaúčtována, i když jsou definovány interunitní debetní a kreditní účty.

Často slýcháme o zákaznících, kteří definují vyrovnávací dimenzi jak v nastavení hlavní knihy, tak v nastavení finanční dimenze. V tomto případě systém využívá funkci finančních dimenzí. Nastavení pro vyvažování dimenzí na úrovni finanční dimenze má při účtování přednost. Zaúčtování se nezdaří, pokud definice účtování nevytvoří vyvážený účetní záznam na úrovni finanční dimenze.

Pomocí těchto kroků zapněte používání vyrovnávací dimenze na úrovni finanční dimenze.

1. Určete, které finanční dimenze budou dimenzemi vyrovnávacími.

    - Jako vyrovnávací dimenzi můžete nastavit více než jednu finanční dimenzi.
    - Ještě nenastavujte finanční dimenze, které budou nutné k vyrovnání transakce na stránce **Finanční dimenze**.

2. Definujte definice účtování pro každý typ deníku nebo zdrojového dokumentu, který používá vaše organizace. Definice účtování spotřebovávají účty hlavní knihy z nezaúčtovaného deníku nebo zdrojového dokumentu jako „kritéria shody“. Definice účtování pak vrátí „vygenerované položky“, které se stanou účetními položkami. Pokud je definice účtování správně nastavena, generovaný záznam obsahuje účty hlavní knihy kritérií shody a další účty k vyrovnání účetního záznamu na úrovni dimenze. Další informace získáte v části [Definice účtování](posting-definitions.md). 
   
   Definice účtování nejsou podporovány u každého typu transakce. Definice účtování například nelze definovat pro žádné transakce zadané prostřednictvím obecného deníku nebo deníku dlouhodobého majetku. Pokud definici účtování nelze definovat pro deník nebo zdrojový dokument, musí být transakce ručně vyvážena na hodnotě finanční dimenze. Pokud je například proveden obecný zápis do deníku a dimenze oddělení je dimenze vyvažování, musíte zajistit, aby každá hodnota oddělení byla v rovnováze.  Pokud dimenze není vyvážená pro každou hodnotu oddělení, poukaz nebude zaúčtován, dokud nebude nerovnováha opravena ručním přidáním interunitního debetu nebo kreditu do voucheru. 

    > [!IMPORTANT]
    > Pokud je nutné ručně vyvážit nadměrný počet transakcí, **neměli** byste použít funkci vyvažovací dimenze na stránce **Finanční dimenze**. Místo toho použijte funkci vyrovnávací dimenze na stránce nastavení **účetní kniha**.

3. Poté, co jsou definice účtování definovány, lze finanční dimenze označit jako požadované pro vyvažování.

Při zadávání a účtování transakcí se během účtování vyvolávají definice účtování, aby se určily účetní záznamy. Pokud jsou finanční dimenze vyvážené, k ověření dojde po určení účetních záznamů. Pokud finanční dimenze nejsou vyvážené, transakce nebude zaúčtována a zobrazí se zpráva, že debety se nerovnají kreditům pro konkrétní dimenzi.
