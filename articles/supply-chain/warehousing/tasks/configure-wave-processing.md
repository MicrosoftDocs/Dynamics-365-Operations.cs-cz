---
title: Příklad konfigurace zpracování vlny
description: Toto téma poskytuje příklad, jak nastavit kritéria, která určují, jaká práce se vygeneruje pro sklad při zpracování vlny, a zda se vlny zpracovávají ručně nebo automaticky.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39c3fecf9250ee89c22003d5dff4ea662c3042e3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572978"
---
# <a name="configure-wave-processing-example"></a>Příklad konfigurace zpracování vlny

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje příklad, jak nastavit kritéria, která určují, jaká práce se vygeneruje pro sklad při zpracování vlny, a zda se vlny zpracovávají ručně nebo automaticky. Podle potřeby určete kritéria nastavením šablon vlny a dotazů, které odpovídají vlně ve vydaných řádcích u prodejní objednávky, výrobní nebo kanbanové zakázce.

## <a name="enable-sample-data"></a>Povolit ukázková data

Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní ukázková data. Dříve než začnete, musíte také vybrat právnickou osobu **USMF**.

## <a name="example-scenario-configure-wave-processing"></a>Příkladový scénář: konfigurace zpracování vlny

Tento příkladový scénář vás provede mnoha různorodými nastaveními, která ovlivňují způsob vytváření, naplnění, zpracování a uvolnění vln.

1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Vlny > Šablony vln**.
1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **Název šablony vlny**. Během nastavení šablony vlny zadáváte pořadí, ve kterém budou šablony párovány s uvolněnými řádky na prodejních objednávkách, výrobních zakázkách nebo kanbanech. Když dojde k uvolnění řádku do skladu nebo do výroby, použije se první šablona vlny, pro kterou se splňují kritéria. Doporučujeme proto umístit šablony s nejkonkrétnějšími kritérii do horní části seznamu. Čím širší kritéria, tím pravděpodobněji řádek splní kritéria, a tím větší šance, že budou řádky přiřazeny k chybné vlně.  
1. Zadejte hodnotu do pole **Popis šablony vlny**.
1. V poli **Lokalita** zadejte nebo vyberte hodnotu. Pokud používáte USMF, můžete vybrat pracoviště 2.  
1. V poli **Sklad** zadejte nebo vyberte hodnotu. Pokud používáte USMF, můžete vybrat sklad 24.  
1. V poli **Automatizovat vytvoření vlny** nastavte hodnotu **Ano**. Vyberte tuto možnost, chcete-li automaticky vytvořit vlnu při vydání prodejní objednávky, výrobní zakázky nebo kanbanu do skladu.  
1. Nastavte možnost **Zpracovat vlnu při uvolnění do skladu** na **Ano**. Vyberte tuto možnost, chcete-li automaticky zpracovat vlnu a vytvořit práci při vydání řádku do skladu.  
1. Nastavte možnost **Automatizovat uvolnění vlny** na hodnotu **Ano**. Chcete-li automaticky uvolnit vlnu, vyberte tuto možnost. Výdej je vytvořen a je k dispozici pro mobilního zařízení.  
1. Nastavte možnost **Přiřadit k otevřeným vlnám** na **Ano**. Řádky jsou přiřazeny k vlně podle filtru dotazu pro šablonu vlny.  
1. Nastavte možnost **Automaticky zpracovat vlnu při dosažení prahové hodnoty** na **Ano**. Tuto možnost vyberte, chcete-li automaticky zpracovat vlnu, pokud její hodnoty dosáhnou prahové hodnoty pro hmotnost, dodávku a řádky uvedené ve skupině polí **Prahové hodnoty vlny**. Tato možnost je k dispozici jen tehdy, je-li v poli **Typ šablony vlny** vybrána možnost **Expedice**.  
1. Nastavte možnost **Automatizovat uvolnění práce doplnění** na hodnotu **Ano**. Výběrem této možnosti můžete vytvořit doplnění podle poptávky a automaticky je vydat. Do šablony vlny musíte přidat metodu doplnění vlny a vytvořit šablonu doplnění pomocí typu **Poptávka vlny**.  
1. Použijte nastavení ve skupině polí **Výchozí hodnoty** pro přiřazení atributů vln. Atributy vlny fungují jako filtry pro omezení druhu položek, které mohou používat vlny. Například můžete určit skupinu položek.  
1. Rozbalte část **Metody** a nastavte akce provedené šablonou vln. Metody šablony vlny umožňují kontrolovat pořadí aktivit, skrze které každá vlna prochází během zpracování. Například můžete mít k dispozici metodu pro doplnění vlny. Při přidání metody se automaticky uvede v odpovídajícím umístění v pořadí kroků. Pokud nastavíte možnost **Automatizovat uvolnění práce doplnění** na hodnotu **Ano**, je třeba přidat metodu doplnění.  
1. Zvolte **Uložit**.
1. Zavřete stránku.
1. Přejděte do nabídky **Řízení skladu > Nastavení > Parametry řízení skladu**.
1. Rozbalte část **Zpracování vlny**.
1. V poli **Skupina dávky zpracování vlny** zadejte nebo vyberte požadovanou hodnotu.
1. Nastavte **Zpracovat vlny v dávce** na hodnotu **Ano**.
1. V poli **Čekat na uzamčení (ms) zadejte číslo**. Zadejte čas v milisekundách, po který se bude v rámci kroku přidělení čekat na systémové prostředky, které jsou uzamčený v dalším kroku přidělení. Při překročení tohoto času nebude vlna zpracována a zobrazí se chybová zpráva.  
1. Zvolte **Uložit**.
1. Zavřete stránku.
1. Přejděte na **Navigační podokno > Moduly > Kontrola výroby > Nastavení > Parametry řízení výroby**.
1. V poli **Uvolnit do skladu** vyberte požadovanou možnost.

    V případě prodejních objednávek a zakázek kanbanu je třeba vyhradit zásoby před vydáním objednávky do skladu. V opačném případě položky nebo řádky přidělení nelze zpracovat ve vlně. Pro výrobní zakázky můžete také využít možnost **Povolit částečnou rezervaci**. Například je to užitečné v případě, kdy vlastníte materiály potřebné k zahájení výroby, a můžete počkat, než budou pro dokončení procesu k dispozici další materiály. Pokud vyberete tuto možnost, je nutné ručně opakovat proces vydání do skladu, jakmile budou k dispozici další materiály.
1. Zavřete stránku.

## <a name="additional-resources"></a>Další prostředky

- [Tvorba a zpracování vln](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
