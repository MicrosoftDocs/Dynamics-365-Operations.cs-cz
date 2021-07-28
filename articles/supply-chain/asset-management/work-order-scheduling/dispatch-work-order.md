---
title: Expedice pracovního příkazu
description: Toto téma vysvětluje, jak expedovat pracovní příkaz v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 344f015b5d2de45e3eca1eb8c0f3b1676da945d2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354149"
---
# <a name="dispatch-work-order"></a>Expedice pracovního příkazu

[!include [banner](../../includes/banner.md)]

 

Pomocí funkce **Expedovat** můžete naplánovat jeden pracovní příkaz nebo úlohy pracovního příkaz pro jednoho pracovníka.

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. V seznamu vyberte pracovní příkaz.

3. Na kartě **Obecné** klikněte na volbu **Expedovat**.

4. V dialogovém okně **Naplánovat pracovní příkaz** vyberte pracovníka v poli **Pracovník**.

5. V poli **Naplánovat hodiny** můžete vložit očekávanou pracovní dobu v případě, že se očekávaná pracovní doba liší od hodin prognózy.

6. V poli **Plánované zahájení** můžete upravit počáteční datum a čas v případě potřeby.

7. Pokud by proces plánování měl zohledňovat omezení kapacity týkající se již naplánovaných zdrojů na jiné úlohy, zkontrolujte, zda jsou přepínací tlačítka **Majetek**, **Nástroj** a **Pracovník** nastavena na hodnotu **Ano**. Chcete-li zobrazit podrobné informace o procesu plánování, vyberte v přepínacím tlačítku **Podrobný** možnost **Ano**. To znamená, že v informačním protokolu budou zobrazeny podrobné informace o vypočteném skóre na pracovním příkazu.

8. Chcete-li ignorovat uzavřené dny v kalendáři (platí pro majetek, pracovníka a nástroje), vyberte možnost **Ano** na přepínacím tlačítku **Ignorvat plán**. Výběrem možnosti **Ano** na přepínacím tlačítku **Ignorovat plánované** provádění můžete ignorovat omezení, která byla vybrána v pracovním příkazu týkajícím se plánování. 

    Informace o nastavení plánovaného provádění naleznete v části [Plánované provádění](../setup-for-work-orders/scheduled-execution.md) section.

9. Klikněte na tlačítko **OK**. Stav životního cyklu pracovního příkazu je automaticky aktualizován do stavu životního **Naplánováno**, který je určen v cestě **Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Modely životního cyklu**.

Na následujícím obrázku je uveden příklad výběru expedice v dialogovém okně **Naplánovat pracovní příkaz**.

![Obrázek č. 1.](media/04-work-order-scheduling.png)

[!NOTE]
Pokud chcete odstranit plán v pracovním příkazu, vyberte pracovní příkaz v možnosti **Všechny pracovní příkazy** a kliknutím možnost **Odstranit plán** na kartě **Obecné** . Nezapomeňte ručně aktualizovat stav životního cyklu pracovního příkazu, pokud jste plán odstranili.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]