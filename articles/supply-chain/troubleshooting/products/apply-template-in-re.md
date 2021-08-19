---
title: Na vydaný produkt nelze použít šablonu
description: Na vydaný produkt nelze použít šablonu.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 566686b6a86e67c87f75f9f2e397592174d3d749034f18997ca8ce651c2594a2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760387"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>Na vytvoření vydaného produktu nelze použít šablonu.

Číslo článku znalostní báze: 4612097

## <a name="symptoms"></a>Příznaky

Když vytvoříte nový vydaný produkt pomocí dialogového okna **Nově vydaný produkt**, můžete vybrat šablonu. Šablona by měla poskytovat výchozí nastavení pro mnoho polí nově vydaného produktu. Některá nebo všechna pole se však po výběru šablony nenastaví.

## <a name="cause"></a>Příčina

Mnoho stránek v Microsoft Dynamics 365 Supply Chain Management vám umožní vytvořit šablonu, která stanoví počáteční nastavení pro záznamy, které se zobrazují na těchto stránkách. Jednu z těchto šablon můžete vytvořit výběrem možnosti **Informace o záznamu** na kartě **Možnosti** v podokně akcí. Vydané produkty jsou však mnohem komplexnější než většina ostatních typů záznamů. I když můžete vybrat **Informace o záznamu** na stránce **Vydané produkty** k vytvoření šablony, a i když tuto šablonu můžete vybrat při vytváření vydaného produktu, šablona neposkytne očekávané hodnoty polí pro nově vydaný produkt. Proto u vydaných produktů nemůžete použít šablony „informace o záznamu“. Místo toho musíte vytvořit vyhrazené šablony produktů.

## <a name="resolution"></a>Rozlišení

Chcete-li vytvořit šablonu produktu, použijte nabídku **Šablona** na kartě **Produkt** podokna akcí, nikoli tlačítko **Informace o záznamu** na kartě **Možnosti**.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. V podokně akcí na kartě **Produkt** ve skupině **Nový** vyberte **Šablona** a pak vyberte **Vytvořit osobní šablonu** nebo **Vytvořit sdílenou šablonu**.
