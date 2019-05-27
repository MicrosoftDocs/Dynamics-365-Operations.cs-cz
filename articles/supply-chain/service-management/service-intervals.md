---
title: Intervaly servisu
description: Servisní interval určuje, jak často jsou pro řádky servisní smlouvy vytvářeny řádky servisní zakázky při automatickém vytváření servisních zakázek.
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10078cbd02209126e9655b823fcf844b692a4794
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562642"
---
# <a name="service-intervals"></a>Intervaly servisu

[!include [banner](../includes/banner.md)]

Interval servisní smlouvy určuje, jak často jsou pro řádky servisní smlouvy vytvářeny řádky servisní zakázky při automatickém vytváření servisních zakázek.

Pokud vytváříte servisní zakázky automaticky, řádky servisní zakázky se vytvářejí podle intervalu, který jste zadali v řádku servisní smlouvy od počátečního data řádku smlouvy.

Pokud je pole **Interval** řádku servisní smlouvy na stránce **Servisní smlouvy** prázdné, řádek představuje jednorázovou událost a nepoužívá se při opakovaném vytváření servisních zakázek.

## <a name="example"></a>Příklad

Tento příklad ukazuje, jaký vliv má interval servisu na řádky servisní smlouvy a servisní zakázky na servisní zakázce.

### <a name="create-a-service-agreement"></a>Vytvoření servisní smlouvy

Nejprve vytvořte servisní smlouvu a nastavte možnost **Kombinace servisních zakázek** na **Podle servisní smlouvy**.

1. Klikněte na **Servisní smlouvy**
2. V **podokně akcí**na kartě **Servisní smlouva** ve skupině **Nová** klikněte na **Servisní smlouva** a vytvořte novou servisní smlouvu.
3. Zadejte popis, vyberte projekt v poli **ID projektu** a zadejte datum do pole **Počáteční datum**.
4. V poli **Kombinace servisních zakázek** vyberte **Podle servisní smlouvy**.

Nyní jste vytvořili následující servisní smlouvu:

| Project      | Počáteční datum                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Váš projekt | Datum, které jste určili pro projekt. V tomto příkladu se používá aktuální datum. |

### <a name="create-a-service-agreement-line"></a>Vytvoření řádku servisní smlouvy

Dále vytvoříte řádek servisní smlouvy s typem transakce **Hodina**.

Pro dokončení této části příkladu musíte vytvořit interval servisu 10 dní na stránce **Servisní intervaly**. 

1. Vyberte servisní smlouvu, kterou jste právě vytvořili. 
2. Na pevné záložce **Řádky** klikněte na tlačítko **Přidat** a vytvořte nový řádek v dolním podokně stránky **Servisní smlouvy**.
3. V poli **Typ transakce** zvolte **Hodina**.
4. V poli **Pracovník** vyberte pracovníka, který dodá servis.
5. V poli **Interval servisu** vyberte interval 10 dní.

Nyní jste vytvořili řádek servisní smlouvy s následujícími informacemi:

| typ transakce | Počáteční datum                               | Interval servisu |
|------------------|------------------------------------------|------------------|
| Hodina             | Aktuální datum.                        | Každých 10 dní    |
| Pracovní podproces           | Pracovník, který provede servis. |                  |

Pro řádek není určené žádné časové okno. 

### <a name="create-planned-service-orders"></a>Vytvoření plánovaných servisních zakázek

Nyní můžete vytvořit plánované servisní zakázky nebo řádky servisních zakázek nadcházející měsíc.

1. Na stránce **Servisní smlouvy** v **podokně akcí** na kartě **Dodat** klikněte na **Plánované servisní zakázky**.
2. Na stránce **Vytváření servisních zakázek** zadejte aktuální datum do pole **Od data** a datum, které je od aktuálního data za měsíc zadejte do pole **Do data**.
3. Nastavte posuvník **Hodina** na **Ano**. 
4. Klikněte na tlačítko **OK**.

Vzhledem k tomu, že servisní zakázka neobsahuje žádné seskupení (definováno možností **Podle servisní smlouvy** v poli **Kombinace servisních zakázek**), pro jednu servisní zakázku je vytvořený jeden řádek.

### <a name="service-orders-created"></a>Vytvořené servisní zakázky

Tři řádky servisních zakázek byly vytvořeny v tomto časovém rozsahu, který jste zadali v dialogovém okně **Vytváření servisních zakázek**. Můžete zobrazit řádky servisní zakázky na stránce **Servisní smlouvy** (**Podokno akcí** \> karta **Dodat** tlačítko \>**Zobrazit**).

## <a name="related-topics"></a>Související témata

[Nastavení intervalů servisu](set-up-service-intervals.md)  

