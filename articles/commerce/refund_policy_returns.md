---
title: Vytvoření a aktualizace zásady vrácení a refundace pro kanál
description: Toto téma vysvětluje, jak nastavit zásady vrácení a refundace pro kanál.
author: ShalabhjainMSFT
ms.date: 07/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 6cb2bb77a62ee9fc2ea6115949e30496bf3365c4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345101"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Vytvoření a aktualizace zásady vrácení a refundace pro kanál

[!include [banner](includes/banner.md)]

Zásada vrácení se změnami kanálu v Dynamics 365 Commerce umožňuje prodejcům nastavit vynucení, na kterých lze úhrady plateb povolit pro zpracování vrácení na pokladním místě (POS).  

Toto téma vysvětluje postup nastavení zásad vrácení a refundace pro kanál.

Rozsah zásady je aktuálně omezen na nastavení nabídek plateb, které lze povolit pro kanál. Seznam povolených položek vychází z metod plateb, které byly použity při nákupu. Například:

- Pokud byl nákup proveden pomocí dárkového poukazu, platí zásady obchodu pro zpracování refundací pouze na nový dárkový poukaz nebo pro poskytnutí dobropisu obchodu. 
- Pokud je prodej uskutečněn s použitím hotovosti, jsou možnosti refundace hotovostní, dárkové poukazy a účet odběratele, ale ne kreditní karta. 

## <a name="enable-return-policy"></a>Povolit zásady vracení

Chcete-li povolit funkci zásad vrácení v rámci prodejního kanálu, postupujte takto:

1. Přejděte do pracovního prostoru **Správa funkcí** v Dynamics 365 Commerce.
1. Vyhledejte v seznamu názvů funkcí funkci **Povolit zásady vracení kanálů**.
1. Vyberte **Povolit**.
1. Na stránce **Harmonogram distribuce** spusťte úlohu **1110** (Globální konfigurace) k distribuci změny funkce. 

## <a name="configure-return-policy"></a>Konfigurace zásad vracení

Chcete-li konfigurovat zásady vracení pro maloobchodní prodejnu nebo online maloobchodní kanál, postupujte podle následujících kroků.

1. Přejděte na **Maloobchodní a velkoobchodní prodej** \> **Nastavení kanálu** \> **Vracení** \> **Zásady vracení v rámci kanálu**.

1. Vyberte **Nová** pro vytvoření nové šablony zásad vracení. Chcete-li použít existující šablonu, vyberte ji v levém podokně. Pro nové šablony přidejte název a popis, který vám pomůže určit zásadu při jejím použití v prodejním kanálu.

   ![Přidat nové zásady vrácení.](media/Return-policy-page1.png)
     
   
1. V části **Povolené způsoby platby refundace** definujte **povolené** nabídky výplat vratek, které jsou specifické pro jednotlivé způsoby platby.
   ![Nastavit povolené metody platby podle typu platby.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - Způsoby platby jsou odvozeny ze způsobů platby nastavených pro organizaci.
    > - Přidání povoleného typu úhrady vratky pro každý ze seznamu způsobu platby zajistí, že vrácení může být provedeno na povolený typ úhrady vratky.
    
1. Přiřaďte šablonu zásad vracení s obchody, kde bude použita. Na kartě **Maloobchodní kanály** vyberte **Přidat** a přidružte dostupné kanály. 

    - V dialogovém okně **Vybrat uzly organizace** vyberte obchody, oblasti a organizace, ke kterým má být daná šablona přidružena.
    - Ke každému obchodu lze přidružit pouze jednu šablonu zásad vracení.
    - Pomocí tlačítek se šipkami vyberte obchody, regiony nebo organizace.
    - Datum začátku platnosti zásady bude datem, kdy jsou zásady použity pro kanály a spouštěné úlohy kanálu. 

    ![Dialogové okno Vybrat organizační uzly.](media/Return-policy-page3.png)

1. Na stránce **Plán distribuce** spusťte úlohu **1070** pro zpřístupnění zásad vracení prodejního kanálu v POS.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Náhled zásad vrácení kanálů v POS

Chcete-li zobrazit povolené typy úhrad vratek v POS, postupujte podle kroků v jednom z následujících příkladů.

1. Přihlaste se k POS jako pokladník nebo manažer.
1. V části **Směna a pokladna** vyberte **Zobrazit deník**.
1. Vyberte transakci, která je součástí vrácení. 
1. Vyberte položky k refundaci a vyberte způsob platby.  
    - Pokud je vybraná úhrada plateb v seznamu povolených typů úhrad vratek, může pokladní dokončit transakci.
    - Není-li vybraná úhrada plateb povolena, zobrazí se chybová zpráva.
    - Chcete-li zobrazit seznam všech povolených typů úhrady vratek, vyberte **Dlužná částka**.

- nebo -

1. Přihlaste se k POS jako pokladník nebo manažer.
1. Vyberte **Transakce vrácení** a zadejte ID účtenky pomocí kontroly čárového kódu nebo ručním zadáním. 
1. Vyberte transakci, která je součástí vrácení. 
1. Vyberte položky k refundaci a vyberte způsob platby.  
    - Pokud je vybraná úhrada plateb v seznamu povolených typů úhrad vratek, může pokladní dokončit transakci.
    - Není-li vybraná úhrada plateb povolena, zobrazí se chybová zpráva.
    - Chcete-li zobrazit seznam všech povolených typů úhrady vratek, vyberte **Dlužná částka**.

![Typ refundace není povolen.](media/Return-policy-page6.png)



![Typy refundace nejsou povoleny.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
