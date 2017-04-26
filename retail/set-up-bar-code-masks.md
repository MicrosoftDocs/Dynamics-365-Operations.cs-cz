---
title: "Nastavení masek čárových kódů"
description: "Toto téma popisuje, jak nastavit znaky masky čárového kódu, masky čárového kódu a jak přiřadit čárový kód masky čárových kódů."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Nastavení masek čárových kódů

[!include[banner](includes/banner.md)]


Toto téma popisuje, jak nastavit znaky masky čárového kódu, masky čárového kódu a jak přiřadit čárový kód masky čárových kódů.

<a name="set-up-bar-code-mask-characters"></a>Nastavení znaků masky čárového kódu
-------------------------------

Masky čárových kódů se používají k vytvoření čárových kódů a rychle identifikovat čárové kódy, které jsou prohledávány do místa prodeje (POS). Masky se skládají ze znaků, které slouží jako zástupné symboly, které označují formát pro čárové kódy, které budou vytvořeny. Chcete-li konfigurovat masku čárového kódu, musíte nastavit znaky masky čárového kódu. Přejít na **maloobchodní a commerce**&gt;**řízení zásob**&gt;**čárové kódy a popisky**&gt;**masky znaky**. Klepněte na tlačítko **nové** k vytvoření znaků masky čárového kódu. Znaky masky je možné vytvořit označují následující data čárového kódu.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Zástupný symbol pro ID produktu.                                                                                     |
| **Any number**       | Slouží k zadání čísla, který bude pevný kódované v čárových kódů.                                                  |
| **Check digit**      | Označuje, že čárový kód formátu v masce čárového kódu používá jako kontrolní číslice pro potvrzení platnosti čárového kódu. |
| **Size digit**       | Označuje velikost v čárovém kódu vytvořit varianty produktu, která zahrnuje velikost.                                 |
| **Color digit**      | Určuje barvu v čárovém kódu vytvořit varianty produktu, který obsahuje barvu.                               |
| **Style digit**      | Určuje styl v čárovém kódu vytvořit varianty produktu, který obsahuje styl.                             |
| **EAN license code** | Zástupný symbol pro EAN licenci vydanou licenční kódy EAN.                                                       |
| **Cena**            | Cena označuje za cenu vložené čárové kódy.                                                                   |
| **Quantity**         | Označuje množství v množství, náhodná hmotnost vložené čárové kódy.                                                |
| **Employee**         | Určuje segment čárový kód pro identifikační číslo zaměstnance, pro přihlášení čárový kód POS.                                  |
| **Customer**         | Označuje ID segmentu zákazníků.                                                                                  |
| **Zadávání dat**       | *Dosud není implementováno.*                                                                                          |
| **Discount code**    | Označuje kód slevy pro čárový kód, který se používá k přidání slevu na místo transakce prodeje             |
| **Dárkový poukaz**        | Označuje číslo dárkového poukazu při vydávání nebo platbě dárkovým poukazem.                                               |
| **Loyalty card**     | Přidá k transakci věrného zákazníka a může být použita při platbě věrnostní.                             |

## <a name="define-bar-code-masks"></a>Definování masky čárového kódu
Po znaky masky čárového kódu jsou určeny pro potřeby čárový kód masky, přejděte k **maloobchodní a commerce**&gt;**řízení zásob**&gt;**čárové kódy a popisky**&gt;**nastavení masky čárového kódu**. Na této stránce můžete definovat masky čárového kódu, které používají dříve zadané znaky. Tyto čárový kód masky budou použity při generování čárových kódů a rovněž pomáhají identifikovat čárové kódy naskenované v POS.

1.  Klepněte na tlačítko **nové** Chcete-li vytvořit novou masku čárového kódu.
2.  Zadejte hodnoty do **ID masky** a **popis** pole a potom vyberte typ masky čárového kódu **typu** pole.
3.  V **Obecné** oddílu, vyberte hodnotu v **standard čárového kódu** pole a potom zadejte prefix čárového kódu, pokud je třeba.
4.  V **segment masky čárového kódu** oddílu, přidat čárový kód segmenty, které budou použity v čárovém kódu, který má být vytvořen.

Například k vytvoření masky čárového kódu s ID masky "Výrobek", je by takto:

1.  Vytvořte novou masku čárového kódu a vyberte typ "Produkt".
2.  Vyberte standardní čárový kód, například kód 39' '.
3.  Zadejte předponu pro snadnou identifikaci čárového kódu. Například "22".
4.  Přidáte segment masky. Segment masky "Výrobek" bude vybrána.
5.  Stanovit délku segmentu produktu, například 10. Délka by měl odpovídat délce kód product ID, který je běžně používán v úložišti. Maska se zobrazí jako náhled v **Obecné** v oddílu **masku**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Přiřadit čárové kódy masek čárových kódů
Masky čárových kódů musí před použitím přiřadit čárové kódy. Pokračovat v předchozím příkladu přiřazení masky čárového kódu čárového kódu, proveďte následující kroky:

1.  Přejít na **Správa organizace**&gt;**nastavení**&gt;**čárové kódy**. Klepněte na tlačítko **nové** vytvořte nový čárový kód.
2.  Zadejte hodnoty do **čárový kód****nastavení** a ** nastavení ** pole.
3.  V **Obecné** oddílu **typ čárového kódu** vyberte 'Kód 39'. V **masky****ID** vyberte dříve vytvořené masce "Výrobek".
4.  Podle **velikost**, zadejte "12".
5.  Click **Save**.

Maska čárového kódu lze nyní vytvářet čárové kódy pro produkty. Výše uvedené kroky jsou příklady vytváření masek čárových kódů pro produkty, ale jsou také ukazují, jak vytvořit masky čárového kódu pro všechny ostatní typy podporovaných čárového kódu. Masky čárových kódů, typy a délky, je třeba upravit pro použití v konkrétním prostředí.




