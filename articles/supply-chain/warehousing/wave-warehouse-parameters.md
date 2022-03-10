---
title: Parametry skladu pro zpracování vlny
description: Toto téma popisuje způsob nastavení skladových parametrů pro zpracování vlny. Zpracování vlny můžete použít k seskupení výdeje pro několik objednávek práce do podoby jedné vlny.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cd7961ae8f4237bcee7ae4c53365d24ab03c5aa9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572211"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Parametry skladu pro zpracování vlny

[!include [banner](../includes/banner.md)]

Toto téma popisuje způsob nastavení skladových parametrů pro zpracování vlny. Zpracování vlny můžete použít k seskupení výdeje pro několik objednávek práce do podoby jedné vlny.

Chcete-li použít zpracování vlny, na stránce **Parametry řízení skladu** zadejte následující:

- Pokud můžete zpracovat vlny v dávkové úloze.
- Pokud shromažďujete informace v souboru protokolu při zpracování vln.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Nastavení parametrů řízení skladu pro zpracování vlny

Pro nastavení parametrů skladu při zpracování vlny postupujte následujícím způsobem:

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Parametry řízení skladu**.

1. Na záložce s náhledem **Zpracování vlny** proveďte následující nastavení:

    - **Skupina dávek pro zpracování vln** – Vyberte skupinu dávek, které chcete použít při zpracování vlny za pomoci dávkových úloh. Skupina dávek určuje server, na kterém budou dávkové úlohy běžet.
    - **Zpracovat vlny v dávce** – Zvolte, zda povolit automatické zpracování vln dávkovou úlohou. Pro použití paralelního zpracování musíte tuto možnost nastavit na *Ano*. Dávkovou úlohu lze nastavit na stránce **Zpracovat vlny**. (Viz také poznámka na konci tohoto seznamu.)
    - **Vytvořit protokol průběhu vlny** – Zvolte, zda má systém generovat záznam protokolu při zahájení a ukončení každého přidělení položky a jejích dimenzí. Tento protokol byste měli povolit, pouze když ho potřebujete, například při počátečním testování nebo při řešení potíží. Další informace získáte v části [Přidělení vlny](wave-allocation-method.md).
    - **Vytvořit protokol historie zpracování vln** – Zvolte, zda se mají automaticky ukládat informace o vlně do souboru protokolu po zpracování vlny, a to i během paralelního zpracování nevyřízených přidělení. Obvykle byste to měli povolit pouze během odstraňování problémů, protože to přidává další režijní náklady. Chcete-li zobrazit protokol, přejděte na **Řízení skladu \> Odchozí vlny \> Protokol historie zpracování vln**. Další informace naleznete v tématu [Vytvoření a zpracování vlny](wave-processing.md).
    - **Vytvořit protokol historie vytváření kontejnerů** – Zvolte, zda se mají po zpracování vlny automaticky ukládat informace o vytváření kontejnerů pro danou vlnu do souboru protokolu. Chcete-li zobrazit protokol, přejděte na **Řízení skladu \> Balení a vytváření kontejnerů \> Historie vytváření kontejnerů**.
    - **Čekat na uzamčení (ms)** – Zadejte čas v milisekundách, po který se bude v rámci kroku přidělení čekat na systémové prostředky, které jsou uzamčeny jiným krokem přidělení. Při překročení tohoto času nebude vlna zpracována a zobrazí se chybová zpráva.

1. Na záložce s náhledem **Uvolnění do skladu** proveďte následující nastavení:

    - **Chyba při selhání dávky** – Zvolte, zda se má generovat chyba, když selže dávková úloha uvolnění do skladu. Pokud je toto povoleno, vadné úlohy skončí ve stavu *Chyba*. Pokud je toto zakázáno, vadné úlohy skončí ve stavu *Ukončeno*.

> [!NOTE]
> V šabloně vlny používané pro zpracování vlny můžete zadat nastavení automatizace zpracování vlny. Je-li nastaven plán pro dávkovou úlohu, je třeba koordinovat časování v rámci nastavení automatizace v šabloně vlny. Další informace naleznete v tématu [Vytvoření šablony vlny](wave-templates.md).
>
> Pokud používáte *Správa přepravy* a *Pokročilé řízení skladu*, můžete určit, zda chcete konsolidovat vytížení při zpracování vlny. To je například užitečné v případě, že lze několik malých nákladů expedovat současně. Chcete-li konsolidovat vytížení při zpracování vlny, na kartě **Vytížení** zaškrtněte políčko **Konsolidovat vytížení během zpracování vlny**.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Nastavení úplné nebo částečné rezervace pro vlny výroby

V případě prodejních objednávek a zakázek kanbanu je třeba vyhradit zásoby před vydáním objednávky do skladu. V opačném případě položky nebo řádky přidělení nelze zpracovat ve vlně. Výrobní zakázky jsou však mírně pružnější. Pro výrobní zakázky můžete zadat následující:

- Povolte vydání výrobních zakázek do skladu, i když nelze mít vyhrazeny všechny materiály. Pokud vyberete tuto možnost, je nutné ručně opakovat proces vydání do skladu, jakmile budou k dispozici další materiály. Například je to užitečné v případě, kdy vlastníte materiály potřebné k zahájení výroby, a můžete počkat, než budou k dispozici další materiály.
- Požadujte, aby byl veškerý materiál vyhrazen před tím, než je možné výrobní zakázku uvolnit do skladu.

Pokud chcete vyžadovat úplnou rezervaci nebo povolit částečnou rezervaci, postupujte takto:

1. Přejděte na **Řízení výroby** \> **Nastavení** \> **Parametry modulu Řízení výroby**.
1. Na kartě **Obecné** v poli **Uvolnit do skladu** vyberte výchozí nastavení.
