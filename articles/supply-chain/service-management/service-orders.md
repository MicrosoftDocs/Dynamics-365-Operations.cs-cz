---
title: Servisní zakázky
description: Servisní zakázka představuje návštěvu servisního technika u zákazníka ve stanovený den.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e9825dbd4ebe05b2efb590f491b3b54e68ec5a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010465"
---
# <a name="service-orders"></a>Servisní zakázky   

[!include [banner](../includes/banner.md)]


Servisní zakázka představuje návštěvu servisního technika u zákazníka ve stanovený den. Každá servisní zakázka se skládá z jednoho nebo více řádků servisní zakázky. Řádky servisní zakázky představují hodiny práce, kterou musí provést servisní technik, a související položky, výdaje a poplatky.

K řádku servisní zakázky můžete připojit úkoly a předměty. Poté můžete seskupit řádky servisní zakázky podle úkolu nebo předmětu. K řádkům servisních zakázek také můžete připojit skladové položky.

## <a name="create-service-orders"></a>Vytváření servisních zakázek

Servisní zakázky jsou vytvářeny na základě servisní smlouvy a řádků obsažených v této smlouvě. Můžete však vytvořit servisní zakázky, které jsou asociovány se servisní smlouvou pouze za období, které je určeno ve smlouvě. Například pokud je servisní smlouva platná pro kalendářní rok 2011, můžete servisní zakázky vytvářet pro smlouvu z 1. ledna 2011 a 31. prosince 2011.

Servisní zakázky lze také vytvořit samostatně jejich přidružení ke smlouvě. Tyto servisní zakázky lze použít ke zpracování neplánovaných nebo jednorázových servisních zásahů. Například v březnu se zákazník rozhodne, že potřebuje nad rámec servisních zásahů, které jsou uvedené v servisní smlouvě, provést servis dvou strojů. Pro tento úkol lze servisní zakázky vytvořit bez jejich přidružení k servisním smlouvám.


> [!NOTE]
> <P>K vytvoření servisních zakázek, které nejsou spojeny se servisní smlouvou, je nutné zaškrtnout políčko <STRONG>Povolit bez servisní smlouvy</STRONG> ve formuláři <STRONG>parametry správy servisu</STRONG>.</P>

**Scénář**

Následující scénář popisuje jinou situaci, kdy je užitečné nejdříve vytvořit servisní zakázku, která není přidružena k servisní smlouvě.

Dispečerka společnosti přijme telefonickou žádost o servis výtahu. Neexistuje žádný čas nastavení servisní smlouvy a projektu služby. Proto dispečerka vytvoří servisní zakázku přímo ve formuláři **servisní zakázky**, připojí servisní zakázku ke stávajícímu projektu a vytvoří řádky servisní zakázky. Kvůli zaznamenání práce, která nesouvisí se servisní smlouvou, může dispečerka vytvořit vztah s úkolem nebo předmětem stávající servisní zakázky. Další informace naleznete v tématu [ruční vytvoření servisních zakázek](create-service-orders-manually.md) a [vytvoření vztahů servisních úloh](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>Sledování průběhu servisních zakázek

Pokud chcete monitorovat pokrok servisní zakázky v různých týmech a pracovních procesech, můžete nastavit systém fází a kódů důvodu servisních zakázek. Pro každou fázi můžete zadat povolené akce: Další informace naleznete v tématu [Vytvoření kódů důvodu](create-reason-codes.md).

**Příklad**

Servisní zakázky je schválena dispečerkou. Ta provede aktualizaci fáze servisní zakázky a uvede kód důvodu, který označuje, že servisní zakázka byla uvolněna pro servisního technika. Technik navštíví zákazníka a realizuje servisní zakázku.

## <a name="specify-item-requirements-for-service-orders"></a>Určení požadavků položky pro servisní zakázky

Můžete určit skladové položky, které jsou požadovány pro servisní zakázky. Servisní zakázka však musí být spojena s projektem. Požadavky zboží pro objednávky služeb jsou zpracovávány prostřednictvím projektu. 

**Příklad**

Servisní zakázky, které jsou vytvořené ze servisních smluv, zpracuje dispečerka. U první servisní zakázky dispečerka zjistí, že servisní technik potřebuje důležitý náhradní díl, který momentálně není na skladě. Vytvoří proto pro náhradní díl požadavek na položku přímo ze servisní zakázky.

## <a name="move-and-post-lines"></a>Přesun a zaúčtování řádků

Servisní technik vrátí servisním zásahu upraví a aktualizuje řádky servisní zakázky. Při servisním zásahu technik provedl servisní úkon, který je naplánován na příští servisní návštěvu. Technik proto přesune řádky z dalšího servisního zásahu do aktuálního servisního zásahu. Technik zaúčtuje servisní zakázku. Další informace o fázích servisní zakázky naleznete v tématu [Přesunutí řádků servisní zakázky](move-service-order-lines.md)..

## <a name="cancel-service-orders"></a>Zrušit servisní zakázky

Jedna ze servisních zakázek, které byly vytvořeny v lednu, je zastaralá, protože servisní zásah byl zrušen. Proto dispečerka tuto servisní zakázku zruší. Další informace o kombinování servisních zakázek naleznete v tématu [Zrušení servisních zakázek](cancel-service-orders.md).

## <a name="post-from-projects"></a>Účtování z projektů

Na konci každého týdne chce dispečerka zaúčtovat všechny servisní zakázky, které jsou připojené k určitému projektu. Proto dispečerka vyhledá příslušný projekt ve formuláři **projekty** a zaúčtuje servisní zakázky, které byly dokončeny. Další informace naleznete v tématu [Zaúčtování servisních zakázek (formulář třídy)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Odstranit servisní zakázky

Ve druhé polovině roku zákazník dospěje k závěru, že servisních zásahů je příliš málo. Pro zbývající dobu servisní smlouvy musíte vytvořit novou sadu častějších servisních zásahů. To znamená, že musíte odstranit stávající servisní zakázky, které již byly vytvořeny (I), a místo nich vytvořit zakázky nové. Další informace naleznete v tématu [Odstranění servisních zakázek](delete-service-orders.md).

## <a name="see-also"></a>Viz také

[Servisní zakázky (formulář)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]