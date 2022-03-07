---
title: Pracovní plocha sestavení vytížení
description: Toto téma popisuje, jak pracovat s pracovní plochou sestavení vytížení.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 306ca4f77d9c1d4879d750992e51c8b83917839e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574850"
---
# <a name="load-building-workbench"></a>Pracovní plocha sestavení vytížení

[!include [banner](../../includes/banner.md)]

Pracovní plocha sestavení vytížení vám umožňuje při vytváření vytížení použít strategie vytváření vytížení.

## <a name="create-a-load-building-strategy"></a>Vytváření strategie sestavení vytížení

Strategie sestavení vytížení používáte k automatickému sestavení vytížení. Tato funkce může být prospěšná v následujících situacích:

- Pokud pravidelně dodáváte konkrétní sadu produktů, strategie vytížení pomáhají šetřit čas, protože nemusíte pokaždé vytvářet stejné vytížení.
- Chcete-li se vyhnout napůl plným vytížením, abyste maximalizovali účinnost, mohou strategie vytížení pomoci naplnit každé vytížení co nejvíce.

Třída strategie sestavení vytížení, která je pojmenována `TMSLoadBuildingVolumeStrategy`, poskytuje strategii sestavení vytížení, která je pojmenována *Strategie sestavení vytížení na základě objemu*. Tato strategie umožňuje použít maximální hodnoty zadané pro výšku a hmotnost v šabloně vytížení nebo přepsat nastavení zadáním nových hodnot. Tato strategie je jedinou strategií, která je zahrnuta ve výchozím nastavení. (Můžete však mít některé vlastní strategie.)

K použití předdefinované strategie *Strategie sestavení vytížení na základě objemu* ji vyberte v poli **Strategie sestavení vytížení** na stránce **Pracovní plocha sestavení vytížení** (**Řízení dopravy &gt; Plánování &gt; Pracovní plocha sestavení vytížení**).

Pro vytvoření strategie sestavení vytížení postupujte podle těchto kroků.

1. Přejděte na **Řízení dopravy &gt; Nastavení &gt; Sestavení vytížení &gt; Strategie sestavení vytížení**.
1. V podokně akcí vyberte **Generovat seznam tříd**, abyste se ujistili, že máte nejnovější verze všech dostupných tříd.
1. V podokně akcí zvolte **Nový**.
1. Zadejte jedinečný název strategie, vyberte pro ni třídu strategie sestavení vytížení a zadejte popis.
1. V podokně akcí vyberte **Uložit**.
1. V podokně akcí zvolte **Parametry**.
1. Na stránce **Parametry strategie sestavení vytížení** vyberte v seznamu možnost **Objemová kapacita**, v poli **Hodnota** zadejte procento z celkové objemové kapacity vytížení, které by se mělo použít pro novou strategii sestavení vytížení.
1. Vyberte v seznamu možnost **Hmotnostní kapacita**, v poli **Hodnota** zadejte procento z celkové hmotnostní kapacity vytížení, které by se mělo použít pro novou strategii sestavení vytížení.
1. Zavřete stránku **Parametry strategie sestavení zatížení**.
1. Zavřete stránku **Parametry sestavení zatížení**.

Nyní můžete strategii sestavení vytížení přiřadit k šabloně sestavení vytížení. Případně ji můžete použít přímo v pracovní ploše sestavení vytížení.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Použití strategie sestavení vytížení na pracovní ploše sestavení vytížení

1. Přejděte do **Správa přepravy &gt; Plánování &gt; Pracovní plocha sestavení vytížení**.
1. Proveďte jeden z následujících kroků:

    - Vyberte strategii v poli **Strategie sestavení vytížení**.
    - Pokud jste definovali šablonu sestavení vytížení a přiřadili k ní strategii pro sestavení vytížení, v podokně akcí na kartě **Správa šablon** vyberte **Použít šablonu**. Pak v rozevíracím dialogovém okně **Použít šablonu sestavení vytížení** vyberte šablonu v poli **Název šablony sestavení vytížení**.

1. Na záložce s náhledem **Řada šablon vytížení** vyberte jednu nebo více [šablon vytížení](load-template.md). Pracovní plocha se pokusí přizpůsobit vytížení do těchto typů kontejnerů v pořadí, které je zde uvedeno. Obvykle byste měli umístit nejmenší kontejnery na začátek seznamu, abyste se ujistili, že je vybrán nejmenší možný kontejner jako první.
1. V podokně akcí klikněte na možnost **Navrhnout vytížení**.
1. Zkontrolujte navrhovaná vytížení a navrhované řádky vytížení.
1. V podokně akcí vyberte **Vytvořit zatížení** a vytvořte vytížení, která jsou založena na řádcích zdrojového dokumentu na záložce s náhledem **Navrhované řádky vytížení**.
1. Zavřete stránku **Pracovní plocha sestavení zatížení**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]