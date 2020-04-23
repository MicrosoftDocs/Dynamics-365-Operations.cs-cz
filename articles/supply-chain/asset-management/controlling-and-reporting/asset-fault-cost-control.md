---
title: Řízení nákladů závad majetku
description: Toto téma popisuje kontrolu nákladů na závady majetku v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bade6ffa5d5a9af6d23d0d681c32e72eb62d4ecc
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205522"
---
# <a name="asset-fault-cost-control"></a>Řízení nákladů závad majetku

[!include [banner](../../includes/banner.md)]

 

V modulu Správa majetku můžete vypočítat náklady na registrace závad majetku pro získání přehledu o skutečných nákladech ve srovnání s rozpočtovými náklady. Skutečné náklady jsou založeny na zaúčtovaných transakcích. Datum je datum závady, kdy byl zaznamenán příznak.

1. Klikněte na **Správa majetku** > **Dotazy** > **Závada majetku** > **Řízení nákladů závad majetku**.

2. V dialogovém okně **Řízení nákladů závad majetku** zvolte sadu finančních dimenzí, která bude v případě potřeby zahrnuta do výpočtu.

4. Nechcete-li zobrazit výsledky obsahující nulové náklady, vyberte možnost Ano na přepínacím tlačítku **Přeskočit nulu**.

5. V poli **Úroveň** určete, jak detailní mají být řádky řízení nákladů v případě funkčních míst. 

    Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky řízení nákladů závad majetku pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni. 
    
    Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky řízení nákladů závad majetku na všech úrovních funkčních míst, ke kterým se vztahují.

6. Chcete-li hledání omezit, můžete vybrat konkrétní majetek, data závad a příčiny závad na záložce s náhledem **Záznamy, které mají být zahrnuty**.

7. Výpočet zahájíte klepnutím na tlačítko **OK**.

8. Ve skupině **Seskupit podle** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu. Vybraná tlačítka **Seskupit podle** jsou zvýrazněna. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

## <a name="example"></a>Příklad

V tomto příkladu je zobrazen výpočet kontroly nákladů majetku.

- V poli **Původní rozpočet** jsou uvedeny rozpočtové náklady z prognózy pracovního příkazu. 
- Pole **Skutečné náklady** zobrazuje zaúčtované náklady na pracovních příkazech. 
- Pole **Potvrzené náklady** zobrazuje celkové množství nákladů, které vaše společnost potvrdila ve vztahu k pracovním příkazům.

    ![Obrázek č. 1](media/05-controlling-and-reporting.png)

Více informací o nastavení závad získáte v části [Správa závad](../setup-for-work-orders/fault-management.md).
