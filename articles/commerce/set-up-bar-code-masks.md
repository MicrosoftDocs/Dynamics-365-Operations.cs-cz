---
title: Nastavení masek čárových kódů
description: Tento článek popisuje, jak nastavit znaky masky čárového kódu a masky čárového kódu a jak přiřadit masky čárového kódu k čárovým kódům.
author: BrianShook
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 97b490384cff27c60191a87dc623eb6a2ef868f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853705"
---
# <a name="set-up-bar-code-masks"></a>Nastavení masek čárových kódů

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak nastavit znaky masky čárového kódu a masky čárového kódu a jak přiřadit masky čárového kódu k čárovým kódům.

## <a name="set-up-bar-code-mask-characters"></a>Nastavení znaků masky čárového kódu

Masky čárových kódů se používají k vytvoření čárových kódů a rychlé identifikaci čárových kódů, které jsou skenovány do pokladního místa (POS). Masky se skládají ze znaků, které slouží jako zástupci označující formát pro čárové kódy, které budou vytvořeny. Chcete-li konfigurovat masku čárového kódu, musíte nastavit znaky masky čárového kódu. Přejděte na **Maloobchodní a velkoobchodní prodej** &gt; **Řízení zásob** &gt; **Čárové kódy a popisky** &gt; **Znaky masky**. Kliknutím na **Nový** vytvořte znaky masky čárového kódu. Znaky masky je možné vytvořit k označení následujících dat čárového kódu.

| Pole            | popis |
|------------------|-------------|
| Produkt          | Zástupce pro ID produktu. |
| Libovolné číslo       | Slouží k zadání čísla, které bude v čárových kódech pevně zakódováno. |
| Kontrolní číslice      | Označuje, že formát čárového kódu v masce čárového kódu používá kontrolní číslici pro potvrzení platnosti čárového kódu. |
| Číslice velikosti       | Označuje velikost v čárovém kódu vytvořeném pro variantu produktu, která zahrnuje velikost. |
| Číslice barvy      | Označuje barvu v čárovém kódu vytvořeném pro variantu produktu, která zahrnuje barvu. |
| Číslice stylu      | Označuje styl v čárovém kódu vytvořeném pro variantu produktu, která zahrnuje styl. |
| Licenční kód EAN | Zástupce pro EAN licenci vydanou pro licenční kódy EAN. |
| Cena            | Označuje cenu pro čárové kódy s vloženou cenou. |
| Množství         | Označuje množství v čárových kódech s vloženým množstvím/hmotností. |
| Zaměstnanec         | Určuje segment čárového kódu pro identifikační číslo zaměstnance používané pro přihlášení k POS pomocí čárového kódu. |
| Zákazník         | Označuje segment ID odběratelů. |
| Zadání dat       | *Není ještě implementováno.* |
| Kód slevy    | *Zastaralé* k verzi Dynamics 365 for Retail z jara 2017. Dříve: Označuje kód slevy pro čárový kód, který se používá za účelem přidání slevy k transakci pokladního místa. |
| Kód kupónu      | Označuje kód kupónu pro čárový kód, použitý pro přidání slevy k prodejní objednávce. T nahradilo kód slevy. |
| Dárkový poukaz        | Označuje číslo dárkového poukazu při vydávání nebo platbě dárkovým poukazem. |
| Věrnostní karta     | Přidá věrného zákazníka k transakci a může být použita při platbě věrnostní kartou. |

## <a name="define-bar-code-masks"></a>Definování masek čárových kódů

Po určení znaků masek čárového kódu pro potřebné masky čárového kódu přejděte na **Maloobchodní a velkoobchodní prodej** &gt; **Řízení zásob** &gt; **Čárové kódy a popisky** &gt; **Nastavení masky čárového kódu**. Na této stránce můžete definovat masky čárového kódu, které používají dříve zadané znaky. Tyto masky čárových kódů budou použity při generování čárových kódů a rovněž pomáhají identifikovat čárové kódy naskenované v POS.

1. Kliknutím na **Nový** vytvořte novou masku čárového kódu.
2. Zadejte hodnoty do polí **ID masky** a **Popis** a potom vyberte typ masky čárového kódu v poli **Typ**.
3. V části **Obecné** vyberte hodnotu v poli **Standard čárového kódu** a potom zadejte předponu čárového kódu, pokud je třeba.
4. V části **Segment masky čárového kódu** přidejte segmenty čárového kódu, které budou použity v čárovém kódu, který má být vytvořen.

Například k vytvoření masky čárového kódu s ID masky "Výrobek", proveďte následující:

1. Vytvořte novou masku čárového kódu a vyberte typ "Produkt".
2. Vyberte standard čárového kódu, například Kód 39.
3. Zadejte předponu pro snadnou identifikaci čárového kódu. Například "22".
4. Přidejte segment masky. Bude vybrán segment masky "Produkt".
5. Stanovte délku segmentu produktu, například 10. Délka by měl odpovídat délce ID produktu, které se běžně používá v obchodu. Maska se zobrazí jako náhled v části **Obecné** pod položkou **Maska**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Přiřaďte masky čárových kódů k čárovým kódům.

Masky čárových kódů musí být před použitím přiřazeny k čárovým kódům. Pokračujte v předchozím příkladu a pro přiřazení masky čárového kódu k čárovému kódu proveďte následující kroky:

1. Přejděte do nabídky **Správa organizace** &gt; **Nastavení** &gt; **Čárové kódy**. Kliknutím na tlačítko **Nový** vytvořte nový čárový kód.
2. Zadejte hodnoty do polí **Nastavení** **čárového kódu** a **Nastavení**.
3. V části **Obecné** v poli **Typ čárového kódu** vyberte 'Kód 39'. V poli **ID** **masky** vyberte dříve vytvořenou masku "Produkt".
4. Do pole **Velikost** zadejte 12.
5. Klikněte na tlačítko **Uložit**.

Masku čárového kódu lze nyní použít k vytvoření čárových kódů pro produkty. Výše uvedené kroky jsou příklady vytváření masek čárových kódů pro produkty, ale také ukazují, jak vytvořit masky čárového kódu pro všechny ostatní podporované typy čárového kódu. Masky čárových kódů, typy a délky je třeba upravit pro použití v konkrétním prostředí.


[!INCLUDE[footer-include](../includes/footer-banner.md)]