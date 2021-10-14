---
title: Vytváření kontejnerů
description: Toto téma popisuje postup automatizace vytváření kontejnerů vytížení. Automatizované vytváření kontejnerů vytvoří kontejnery a práci výdeje pro dodávky při zpracování vlny.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9293beba6a251a670b918fecbb2315a5e94660b9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572258"
---
# <a name="containerization"></a>Vytváření kontejnerů

[!include [banner](../includes/banner.md)]

Toto téma popisuje postup automatizace vytváření kontejnerů vytížení. Automatizované vytváření kontejnerů vytvoří kontejnery a práci výdeje pro dodávky při zpracování vlny.

Chcete-li nastavit tvorbu kontejnerů, je nutné vytvořit následující:

- **Typ kontejneru** – Určuje fyzické vlastnosti kontejnerů. Pomocí typů kontejnerů zabalte položky zásob do určitého typu a velikost balení, jako jsou například přihrádky nebo palety.
- **Skupiny kontejnerů** – Tvorba skupin typů kontejneru, které jsou podobné. Skupina kontejnerů může například zahrnovat typy kontejnerů, které mají podobné rozměry. Skupina kontejnerů určuje pořadí, ve kterém jsou kontejnery zabaleny a procento naplnění každého kontejneru.
- **Šablona sestavení kontejneru** – Vytvořte šablony, které definují pravidla vytváření kontejnerů. Například pravidla pro smíšení zásob a dalších strategií balení.
- **Šablony vlny** – Nastavení jedné nebo více šablon vlny pro vytvoření práce výdeje pro rozdělení do kontejnerů.

## <a name="create-wave-templates-for-containerization"></a>Vytvoření šablon vlny pro vytváření kontejnerů

Musíte nastavit jednu nebo více šablon vlny expedice pro vytváření kontejnerů. Šablony vlny zahrnují kritéria, která určují následující:

- Způsob zpracování vln. To může být ruční nebo automatické.
- Způsob tvorby práce výdeje. To je určeno metodami vlny. Šablona vlny musí zahrnovat metodu **vytváření kontejnerů**.
- Postup párování položek nebo přidělení řádků k vlně.

Další informace naleznete v tématu [Šablony vlny](wave-templates.md).

## <a name="create-container-types"></a>Vytváření typů kontejneru

Typy kontejneru slouží k vytváření popisů kontejnerů, včetně maximálních hodnot pro fyzické rozměry a kapacitu hmotnosti. Při zpracování kontejnerové vlny se kontejnery vytvářejí na základě informací pro typ kontejneru.

Chcete-li nastavit typ kontejneru, postupujte podle následujících pokynů:

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Typ kontejneru**.
1. Zvolte **Nový** pro vytvoření nového typu kontejneru.
1. Zadejte jedinečný identifikátor (ID) a popis typu kontejneru.
1. V poli **Hmotnost obalu** zadejte skutečnou nebo odhadovanou hmotnost kontejneru.
1. Do pole **Maximální hmotnost** zadejte maximální hmotnost, kterou může kontejner pojmout.
1. Do polí **Maximální objem kontejneru**, **Maximální délka kontejneru**, **Maximální šířka kontejneru** a **Maximální výška kontejneru** zadejte fyzické rozměry kontejneru.

    > [!NOTE]
    > Hodnoty pro délku a šířku jsou zaměnitelné. To znamená, že položky lze otáčet laterálně nebo, v případě potřeby, podle osy x. Například, pokud délka je 2 stopy a šířka 1 stopa, můžete změnit délku na 1 stopu a šířku na 2 stopy. Všimněte si, že to neplatí pro dimenzi výšky. Hodnotu výšky nelze změnit ke svislému otáčení položky.

1. Vyberte vlastní hodnoty atributu pro kontejnery v polích pro atributy. Atributy jsou vlastní hodnoty, které slouží k filtrování a řazení položek na základě hodnoty, která není jinak k dispozici. Například pokud chcete balit položky pro konkrétního odběratele, můžete vytvořit atribut pro jméno odběratele. Na stránce **Atributy kontejneru** můžete vytvořit atributy.

## <a name="create-container-groups"></a>Vytváření skupin kontejnerů

Můžete nastavit skupiny kontejnerů logických skupin. Pro každou skupinu můžete určit pořadí, v němž dojde k zabalení kontejnerů, a vyžadované procento naplnění kontejnerů. Dimenze velikosti položky určuje, zda se vejde do kontejneru. Použije se kontejner, který nejlépe odpovídá dimenzím velikosti. Pokud máte více typů kontejnerů ve skupině, doporučujeme, abyste uspořádali pořadí podle velikosti tak, aby největší kontejner byl první (číslo 1 v číselné řadě) a nejmenší kontejner byl poslední.

Chcete-li vytvořit skupinu kontejnerů, postupujte podle následujících pokynů:

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Skupiny kontejnerů**.
1. Zvolte **Nový** pro vytvoření nové skupiny kontejnerů.
1. Zadejte jedinečné ID a popis skupiny kontejneru.
1. Na záložce s náhledem **Podrobnosti** volbou **Nová** přidáte typ kontejneru do skupiny.
1. V poli **typ kontejneru** zadejte typ kontejneru.
1. Volbou **Přesunout nahoru** nebo **Přesunout dolů** určete pořadí, ve kterém jsou zabaleny typy kontejnerů.

## <a name="create-container-build-templates"></a>Vytváření šablon sestavení kontejneru

Můžete nastavit pravidla pro vytváření kontejnerů, například smíšená pravidla zásob nebo další strategie balení. Například můžete vytvořit pravidlo tak, aby pracovníci nemohli zabalit řádky přidělení, které představují prodejní objednávky od různých odběratelů ve stejném kontejneru.

Chcete-li vytvořit šablonu sestavení kontejneru, postupujte podle následujících pokynů.

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Šablona sestavení kontejneru**.
1. Vytvořte novou šablonu sestavení kontejneru.
1. Do polí **Název vytváření kontejnerů** a **Pořadové číslo** zadejte název šablony pro vytváření kontejnerů a pořadí, které odpovídá řádkům přidělení.

    > [!NOTE]
    > Systém použije první šablonu, jejíž řádek přidělení splňuje kritéria dotazu. Proto umístěte šablonu s nejkonkrétnějšími kritérii do horní části seznamu. Čím širší kritéria, tím větší je pravděpodobnost, že řádek přidělení bude odpovídat kritériím. To může vést k přiřazení řádků ke špatnému kontejneru. V případě potřeby můžete volbami **Přesunout nahoru** nebo **Přesunout dolů** změnit pořadí šablon.

1. V poli **ID skupiny kontejnerů** vyberte skupinu kontejnerů ze kterých můžete vytvořit kontejnery.
1. V poli **Základní typy dotazů** vyberte typ dotazu, který určuje, co bude zabaleno, a na čem založit dotaz filtru. Existují tyto možnosti:

      - **Řádek přidělení prodeje** – Řádky přidělení balení, které jsou vytvořeny pro prodejní objednávky.
      - **Řádek přidělení převodu** – Řádky přidělení balení, které jsou vytvořeny pro převodní příkazy.
      - **Kontejner** – Zabalení kontejneru, který již byl vytvořen pomocí procesu vytváření kontejnerů. To se používá například ke vnoření kontejnerů.

        > [!NOTE]
        > Chcete-li používat vnořené kontejnery, musíte učinit metodu tvorby kontejnerů opakovatelnou. Další informace naleznete v tématu [Šablony vlny](wave-templates.md).

1. Na záložce s náhledem **Obecné** v poli **Kód kroku vlny** zadejte jedinečný identifikátor metody zpracování vlny, která propojuje šablonu sestavení kontejneru ke krokům v šabloně vlny.
1. Zaškrtnutím políčka **Povolit rozdělení výdeje** umožníte pracovníkům zabalit položky z pracovních činností do samostatných kontejnerů. To vyžaduje, aby celé množství bylo možné umístit do kontejneru. Nejvyšší měrná jednotka v řádku přidělení se používá vždy.
1. V poli **Zabalit podle jednotky** vyberte jednotku měření, která bude představovat kontejner. Jako kontejner můžete označit,například případ. Pokud použijete zabalení podle měrné jednotky, nemůžete zároveň zadat skupinu kontejnerů, protože měrná jednotka je kontejner.
1. V poli **Strategie balení kontejneru** vyberete strategii balení, která se má použít. Existují tyto možnosti:

    > [!NOTE]
    > Strategie platí pouze pro řádky přidělení prodeje a řádky přidělení převodu.

      - **Zabalit do všech otevřeních kontejnerů** – Systém vyhodnotí, zda se řádek přidělení vejde do některého z kontejnerů vytvořených v průběhu cyklu vytváření kontejnerů.
      - **Zabalit pouze do aktuálního kontejneru** – Systém pouze vyhodnotí, zda se řádek přidělení vejde do naposledy vytvořeného kontejneru.

    Další informace a příklady, které ukazují, jak pracovat se strategiemi balení kontejnerů, najdete v tématu [Strategie balení kontejnerů](container-packing-strategy-overview.md).

1. Pokud chcete v kontejnerech vytvořit pravidla pro řádky přidělení balení, vyberte **Přerušení smíšené logiky**. Můžete například vytvořit pravidlo, které pracovníkům povolí řádky přidělení balení pro dvě různé položky ve stejném kontejneru. Chcete-li definovat pravidlo smíšení, postupujte takto:

    1. Na stránce **Přerušení smíšené logiky** vyberte **Nová**.
    1. V poli **Tabulka** vyberte tabulku obsahující pole použité jako kritérium pro přerušení smíšené logiky.
    1. V poli **Výběr pole** vyberte pole, které chcete použít jako kritérium pro přerušení smíšené logiky.
    1. Opakujte tento postup, dokud nepřidáte všechna kritéria pro přerušení smíšené logiky.

    > [!NOTE]
    > Pokud používáte smíšení logiky, doporučujeme seřadit stejná pole v dotazu kritéria filtru. Tím snížíte počet kontejnerů, které jsou vytvořeny.
