---
title: Vytvoření sestav spotřeby
description: Toto téma vysvětluje, jak vytvořit sestavy spotřeby v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8add0602e0ebe7a5c0cf2c76de6fa2f4f21a2f72
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837914"
---
# <a name="create-consumption-reports"></a>Vytvoření sestav spotřeby

[!include [banner](../../includes/banner.md)]

 

Pokud jste vytvořili a zaúčtovali registrace spotřeby na pracovních příkazech ve správě majetku, budou k dispozici dvě sestavy pro zobrazení podrobností o spotřebě.


## <a name="asset-consumption-report"></a>Sestava spotřeby majetku

Pokud jste zaúčtovali spotřebu v pracovních příkazech, můžete vytisknout sestavu spotřeby majetku. V sestavě jsou uvedeny hodiny, hodinové náklady, náklady na položku a výdaje zaúčtované v majetku.

1. Klikněte na **Správa majetku** > **Sestavy** > **Majetek** > **Spotřeba majetku**.

2. V dialogovém okně **Spotřeba majetku** vyberte parametry a úroveň podrobností, které chcete zobrazit, výběrem možnosti **Ano** na příslušných přepínačích a vložením úrovně funkčního místa do sekce **Zobrazit**.
    - V poli **Úrovně** určete, jak detailní mají být řádky majetku v případě funkčních míst. 
    
        Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny majetky pro funkční místo, a proto lze řádek navýšit z funkčních míst na nižší úrovni. 
        
        Pokud do pole **Úrovně** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechnymajetky na všech úrovních funkčních míst, ke kterým se vztahují. 
        
    - Chcete-li zobrazit součty jednotlivých dílčích majetků v sestavě, vyberte možnost **Ano** na přepínači **Součet na veškerém dílčím majetku**.

3. V části **Data** vyberte časový interval.

4. Na záložce s náhledem **Cíl** vyberte, zda chcete sestavu zobrazit na obrazovce, vytisknout nebo ji uložit jako soubor nebo e-mail.

5. V případě potřeby můžete vybrat konkrétní majetek, který se má v sestavě zobrazit. Na záložce s náhledem **Záznamy k zahrnutí** klikněte na možnost **Filtr** a přidejte majetek, který chcete zahrnout do sestavy.

6. Klepnutím na tlačítko **OK** sestavu vygenerujte.


## <a name="work-order-consumption-report"></a>Sestava spotřeby pracovního příkazu

Pokud jste zaúčtovali spotřebu v pracovních příkazech, můžete vytisknout sestavu spotřeby pracovního příkazu. V sestavě jsou uvedeny hodiny, hodinové náklady, náklady na položku a výdaje zaúčtované na pracovním příkazu.

1. Klikněte na možnost **Správa majetku** > **Sestavy** > **Pracovní příkazy** > **Spotřeba pracovních příkazů**.

2. V dialogovém okně **Spotřeba pracovního příkazu** vyberte parametry, které chcete zahrnout do sestavy, výběrem možnosti **Ano** v příslušných přepínacích tlačítkách v části **Zobrazit**.

3. V části **Data** vyberte časový interval.

4. Na záložce s náhledem **Cíl** vyberte, zda chcete sestavu zobrazit na obrazovce, vytisknout nebo ji uložit jako soubor nebo e-mail.

5. V případě potřeby můžete vybrat konkrétní pracovní příkazy, které se mají v sestavě zobrazit. Na záložce s náhledem **Záznamy k zahrnutí** klikněte na možnost **Filtr** a přidejte pracovní příkazy, které chcete zahrnout do sestavy.

6. Klepnutím na tlačítko **OK** sestavu vygenerujte.


>[!NOTE]
>Můžete také vygenerovat [sestavu pracovních příkazů](../work-orders/work-order-report.md), která obsahuje další podrobnosti o pracovním příkazu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]